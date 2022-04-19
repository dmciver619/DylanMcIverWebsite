<template>
    <div id="title">
        <div ref="titleSvg" class="svg-container">
            <!-- I crated SVG with: https://codepen.io/anthonydugois/pen/mewdyZ -->
            <svg :viewBox="viewBoxSize" class="svg">
                <path ref="curve" fill="#D6994C" :d="curve">
                </path>
            </svg>
        </div>

        <div class="container py-5 page-title" style="background-position: center">
            <h1 class="display-1">Dylan McIver</h1>
            <h3>.NET Full Stack Software Engineer</h3>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'TitleArea',
        mounted() {
            window.addEventListener('scroll', this.animate);
            window.addEventListener('resize', this.resizeSvg);
        },
        beforeUnmount() {
            window.removeEventListener('scroll', this.animate);
            window.removeEventListener('resize', this.resizeSvg);
        },
        data() {
            return {
                last_known_scroll_position: 0,
                viewBoxSize: '0 0 800 600',
                defaultCurveValue: 350,
                curveRate: 3,
                ticking: false,
                curveValue: 350,
                curve: this.calculateCurvePath()
            };
        },
        methods: {
            isOnScreen: function () {
                var titleYPos = this.$refs.titleSvg.offsetHeight;
                var scrollPos = window.scrollY;

                return scrollPos <= titleYPos;
            },
            animate: function () {
                if (!this.isOnScreen()) {
                    return;
                }

                if (window.scrollY >= 0) {
                    this.curveValue = this.defaultCurveValue - (window.scrollY / this.curveRate);
                    this.resizeSvg();
                }
            },
            resizeSvg: function () {
                this.viewBoxSize = '0 0 ' + (window.innerWidth * 0.5) + ' ' + (window.innerHeight * 0.6)
                this.curve = this.calculateCurvePath();
            },
            calculateCurvePath: function () {
                var wallHeight = window.innerHeight * 0.3;
                var wallWidth = window.innerWidth * 0.5;

                var curvePath = 'M ' + wallWidth + ' ' + wallHeight
                    + ' Q ' + (wallWidth * 0.5) + ' ' + this.getCurveValue() + ' 0 ' + wallHeight
                    + ' L 0 0 '
                    + ' L ' + wallWidth + ' 0'
                    + ' L ' + wallWidth + ' ' + wallHeight
                    + ' Z';

                return curvePath;
            },
            getCurveValue: function () {
                return this.curveValue
                    ? this.curveValue
                    : 350;
            }
        }
    }
</script>

<style lang="scss" scoped>

    #title {
        padding-bottom: 200px;
    }

    .container {
        text-align:center;
        background: none;
    }

    .svg-container {
        position: absolute;
        top: 0;
        right: 0;
        left: 0;
        z-index: -1;
        background-color: #090909;
        padding-bottom: 200px;
    }

    svg {
        path {
            transition: .1s;
        }

    }
</style>