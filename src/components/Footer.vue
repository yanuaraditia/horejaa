<template>
    <section class="section my-footer">
        <div class="container is-fluid">
            <div class="columns is-flex is-multiline">
                <div class="column is-12-mobile is-8-desktop">
                    <ul class="footer-link">
                        <li><g-link to="/about">Tentang Kami</g-link></li>
                        <li v-if="isShare"><a href="" type="button" @click="shareLink()">Bagikan</a></li>
                        <li><a href="#">Kontak</a></li>
                        <li><a href="#">Terms of Use</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                    </ul>
                    <p>Copyright &copy; 2020 by <strong>Palagan Food Supplier</strong></p>
                </div>
                <div class="column is-12-mobile is-4-desktop">
                    <ul class="footer-social">
                        <li>
                            <a href="#">
                                <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
                                width="30px" height="30px" viewBox="0 0 30 30" style=" fill:currentColor;">    <path d="M15,3C8.373,3,3,8.373,3,15c0,6.016,4.432,10.984,10.206,11.852V18.18h-2.969v-3.154h2.969v-2.099c0-3.475,1.693-5,4.581-5 c1.383,0,2.115,0.103,2.461,0.149v2.753h-1.97c-1.226,0-1.654,1.163-1.654,2.473v1.724h3.593L19.73,18.18h-3.106v8.697 C22.481,26.083,27,21.075,27,15C27,8.373,21.627,3,15,3z"></path></svg>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
                                width="30px" height="30px" viewBox="0 0 30 30" style=" fill:currentColor;">    <path d="M15,3C8.373,3,3,8.373,3,15c0,6.627,5.373,12,12,12s12-5.373,12-12C27,8.373,21.627,3,15,3z M21.464,12.535 c0.006,0.133,0.009,0.265,0.009,0.397c0,4.068-3.095,8.756-8.756,8.756c-1.739,0-3.356-0.509-4.717-1.383 c0.241,0.029,0.486,0.042,0.735,0.042c1.443,0,2.769-0.491,3.821-1.318c-1.347-0.025-2.484-0.915-2.875-2.137 c0.188,0.036,0.381,0.055,0.579,0.055c0.281,0,0.554-0.038,0.811-0.108c-1.408-0.282-2.469-1.526-2.469-3.017 c0-0.013,0-0.026,0-0.039c0.415,0.231,0.889,0.369,1.394,0.385c-0.825-0.551-1.369-1.494-1.369-2.561 c0-0.565,0.151-1.094,0.416-1.547c1.518,1.862,3.786,3.088,6.343,3.216c-0.052-0.225-0.079-0.46-0.079-0.701 c0-1.699,1.378-3.078,3.077-3.078c0.885,0,1.685,0.374,2.246,0.972c0.701-0.139,1.36-0.394,1.955-0.747 c-0.23,0.719-0.718,1.321-1.354,1.703c0.622-0.074,1.215-0.239,1.768-0.484C22.588,11.559,22.067,12.1,21.464,12.535z"></path></svg>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
                                width="30" height="30" viewBox="0 0 30 30" style=" fill:currentColor;">    <path d="M 9.9980469 3 C 6.1390469 3 3 6.1419531 3 10.001953 L 3 20.001953 C 3 23.860953 6.1419531 27 10.001953 27 L 20.001953 27 C 23.860953 27 27 23.858047 27 19.998047 L 27 9.9980469 C 27 6.1390469 23.858047 3 19.998047 3 L 9.9980469 3 z M 22 7 C 22.552 7 23 7.448 23 8 C 23 8.552 22.552 9 22 9 C 21.448 9 21 8.552 21 8 C 21 7.448 21.448 7 22 7 z M 15 9 C 18.309 9 21 11.691 21 15 C 21 18.309 18.309 21 15 21 C 11.691 21 9 18.309 9 15 C 9 11.691 11.691 9 15 9 z M 15 11 A 4 4 0 0 0 11 15 A 4 4 0 0 0 15 19 A 4 4 0 0 0 19 15 A 4 4 0 0 0 15 11 z"></path></svg>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
export default {
    data() {
        return {
            isShare: false
        }
    },
    computed: {
        webShareApiSupported() {
            return navigator
        }
    }
}
</script>