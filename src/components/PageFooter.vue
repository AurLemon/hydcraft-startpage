<template>
    <footer :class="{ main: showMain }">
        <div class="hydstart-footer">
            <div class="hydstart-footer-register">
                <img src="@/assets/images/logo_mps_register.png" alt="备案">
                ICP 备案号:
                <span class="hydstart-footer-register__icp">
                    <a href="https://beian.miit.gov.cn/">
                        闽ICP备2023007345号-1
                    </a>
                </span>
                <span class="hydstart-footer-register__mps">
                    <a href="https://www.beian.gov.cn/portal/registersysteminfo?recordcode=35010202001677">
                        闽公网安备35010202001677号
                    </a>
                </span>
            </div>
            <div class="hydstart-footer-desc">氢气工艺标志登记于国家版权局，本站由 AurLemon 基于 Vue.js 和 ThinkPHP 设计。我们欢迎所有想与我们交流技术的网友，我们相信：代码改变世界！</div>
            <div class="hydstart-footer-copyright">Copyright © 2018 - 2024 Hydrlab Studio. All Rights Reserved. 氢气实验室 版权所有</div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'PageFooter',
        props: {
            showMain: {
                type: Boolean,
                default: false
            }
        }
    }
</script>

<style lang="scss" scoped>
    @use "sass:math";

    @import '@/assets/styles/global.scss';

    footer {
        $footer-value-transition-duration: 250ms;
        $footer-value-margin: 10rem;
        position: fixed;
        left: 0;
        right: 0;
        bottom: 0;
        z-index: $page-fixed-value-z-index;
        color: var(--color-surface-4);
        font-size: 12px;
        margin: auto $footer-value-margin 0.75rem $footer-value-margin;
        transition: color $footer-value-transition-duration $value-transition-function, text-shadow $footer-value-transition-duration $value-transition-function;

        &.main {
            color: var(--color-surface-1);
            text-shadow: 0 1px 2px var(--color-surface-4);
        }
    }

    .hydstart-footer-register {
        display: flex;
        align-items: center;

        img {
            $image-length: 13px;
            display: block;
            width: $image-length;
            height: $image-length;
            margin-right: 4px;
            user-select: none;
        }

        [class^="hydstart-footer-register__"] {
            margin-left: 4px;
        }
    }

    a {
        color: inherit;

        &:hover {
            color: var(--color-primary);
        }
    }
</style>