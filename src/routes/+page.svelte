<script>
    import { onMount } from "svelte";
    import { onDestroy } from "svelte";

    function backToTop() {
        window.scrollTo({
            top: 0,
            behavior: "smooth",
        });
    }

    let hue = 0;

    function hueShift() {
        console.log("debug");
        if (hue >= 360) {
            hue = 0;
        }
        hue += 30;
        document.documentElement.style.setProperty("--bgHue", hue);
    }
</script>

<main>
    <div class="section" id="section1">
        <div class="card" id="primary">
            <h1 class="header">This is the next big thing.</h1>
            <p class="content">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Unde
                officia quas doloremque culpa incidunt? Repellendus natus,
                accusamus dolore excepturi ullam et tenetur a? Nisi nemo quam
                aut perspiciatis deserunt laborum nostrum iste qui magni,
                placeat temporibus asperiores magnam consequuntur voluptatibus
                mollitia animi id maiores omnis possimus reiciendis repellat
                eaque ab fugit. Deserunt dolore atque facilis molestias
                consequuntur sint impedit adipisci voluptatum non ratione
                ducimus blanditiis quo quae nam sapiente unde vitae rerum libero
                eveniet dolor, hic necessitatibus ad eaque corporis!
                Voluptatibus tempore laborum, architecto unde consectetur sed,
                quos molestiae repudiandae deleniti mollitia labore officiis
                quia aspernatur illo optio beatae nihil!
            </p>
            <p class="content emphasized">This is an important line.</p>
            <p class="content">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam
                corrupti soluta obcaecati reprehenderit dolorum quisquam omnis
                molestiae laboriosam sequi consectetur, neque ducimus
                perferendis, excepturi eius repellendus perspiciatis numquam
                tempora molestias, necessitatibus similique voluptate!
                Consequuntur odio sapiente nemo iste natus est voluptatem quos
                praesentium, eveniet aut modi eligendi aliquam doloremque
                adipisci dolores esse! Placeat quas asperiores ipsa. Cumque
                accusamus aliquid expedita saepe, ab, dolorum aut corrupti ipsum
                tempore facere alias voluptatem ipsam fugiat rerum! Quidem
                itaque officiis dignissimos, dolore animi aliquid architecto,
                corporis possimus dolores eveniet esse vero ullam cumque
                expedita eos odio eius porro repellendus praesentium, voluptas
                quae inventore. Suscipit atque unde vel asperiores
                necessitatibus inventore modi obcaecati, repellat quia.
                Excepturi, maiores expedita dolore quos, totam sunt distinctio
            </p>
        </div>

        <div class="bottomwave">
            <svg
                data-name="Layer 1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 1200 120"
                preserveAspectRatio="none"
            >
                <path
                    d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z"
                    opacity=".10"
                    class="shape-fill"
                />
                <path
                    d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z"
                    opacity=".25"
                    class="shape-fill"
                />
                <path
                    d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z"
                    class="shape-fill"
                />
            </svg>
        </div>
    </div>
    <div class="section" id="section2">
        <div class="topwave">
            <svg
                data-name="Layer 1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 1200 120"
                preserveAspectRatio="none"
            >
                <path
                    d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z"
                    opacity=".10"
                    class="shape-fill"
                />
                <path
                    d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z"
                    opacity=".25"
                    class="shape-fill"
                />
                <path
                    d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z"
                    class="shape-fill"
                />
            </svg>
        </div>
        <div class="card" id="secondary">
            <h1 class="header">Change the Universe</h1>
            <p class="content">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Atque
                nesciunt debitis nisi saepe animi! Eos recusandae quisquam nemo
                quia molestias tempore et, repellat soluta corrupti, impedit
                iusto aut fugit quibusdam voluptas in eveniet? Vel magni tenetur
                unde! Debitis eligendi unde deleniti fuga voluptate nisi iste
                minus id, deserunt modi animi!
            </p>

            <div class="bottomwave">
                <svg
                    data-name="Layer 1"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 1200 120"
                    preserveAspectRatio="none"
                >
                    <path
                        d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z"
                        opacity=".10"
                        class="shape-fill"
                    />
                    <path
                        d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z"
                        opacity=".25"
                        class="shape-fill"
                    />
                    <path
                        d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z"
                        class="shape-fill"
                    />
                </svg>
            </div>
        </div>
    </div>
    <div class="section" id="section3">
        <div class="topwave">
            <svg
                data-name="Layer 1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 1200 120"
                preserveAspectRatio="none"
            >
                <path
                    d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z"
                    opacity=".10"
                    class="shape-fill"
                />
                <path
                    d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z"
                    opacity=".25"
                    class="shape-fill"
                />
                <path
                    d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z"
                    class="shape-fill"
                />
            </svg>
        </div>
        <div class="card" id="primary">
            <h1 class="header">Used by Professional Doctors</h1>
            <div class="imagecontent">
                <div class="portrait">
                    <img
                        alt="doctor"
                        src="https://cdn.discordapp.com/attachments/949834583946457168/1148754059029913700/dr3.png"
                    />
                </div>
                <div class="portrait">
                    <img
                        alt="doctor"
                        src="https://cdn.discordapp.com/attachments/949834583946457168/1148754059843620904/dr1.png"
                    />
                </div>
                <div class="portrait">
                    <img
                        alt="doctor"
                        src="https://cdn.discordapp.com/attachments/949834583946457168/1148754058711158855/dr4.png"
                    />
                </div>
                <div class="portrait">
                    <img
                        alt="doctor"
                        src="https://cdn.discordapp.com/attachments/949834583946457168/1148754059281567774/dr2.png"
                    />
                </div>
                <div class="portrait">
                    <img
                        alt="doctor"
                        src="https://cdn.discordapp.com/attachments/949834583946457168/1148754060296593408/dr5.png"
                    />
                </div>
            </div>
        </div>
        <div class="bottomwave">
            <svg
                data-name="Layer 1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 1200 120"
                preserveAspectRatio="none"
            >
                <path
                    d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z"
                    opacity=".10"
                    class="shape-fill"
                />
                <path
                    d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z"
                    opacity=".25"
                    class="shape-fill"
                />
                <path
                    d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z"
                    class="shape-fill"
                />
            </svg>
        </div>
    </div>
    <div class="section" id="section4">
        <div class="topwave">
            <svg
                data-name="Layer 1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 1200 120"
                preserveAspectRatio="none"
            >
                <path
                    d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z"
                    opacity=".10"
                    class="shape-fill"
                />
                <path
                    d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z"
                    opacity=".25"
                    class="shape-fill"
                />
                <path
                    d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z"
                    class="shape-fill"
                />
            </svg>
        </div>
        <div class="card" id="secondary">
            <h1 class="header">Tiers</h1>
            <div id="container">
                <div class="tier" id="dirt">
                    <span class="subheader">Dirt</span>
                    <ul>
                        <li>512MB RAM</li>
                        <li>Intel Celeron</li>
                        <li>1GB HDD</li>
                        <li>$1/month</li>
                    </ul>
                    <button class="subscribeButton">Subscribe</button>
                </div>
                <div class="tier" id="stone">
                    <span class="subheader">Stone</span>
                    <ul>
                        <li>1GB RAM</li>
                        <li>Intel Pentium</li>
                        <li>10GB HDD</li>
                        <li>$100/month</li>
                    </ul>
                    <button class="subscribeButton">Subscribe</button>
                </div>
                <div class="tier" id="diamond">
                    <!-- svelte-ignore missing-declaration -->
                    <!-- svelte-ignore a11y-click-events-have-key-events -->
                    <!-- svelte-ignore a11y-no-static-element-interactions -->
                    <span class="subheader">Diamond</span>
                    <ul>
                        <li>8GB RAM</li>
                        <li>Intel Core i3</li>
                        <li>100GB HDD</li>
                        <li>$1000/month</li>
                    </ul>
                    <button class="subscribeButton" on:click={hueShift}
                        >Subscribe</button
                    >
                </div>
            </div>
        </div>
    </div>
    <link
        rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0"
    />
    <circle
        cx="100"
        cy="50"
        r="40"
        stroke="black"
        stroke-width="2"
        fill="none"
    />
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <span class="material-symbols-outlined" id="topbutton" on:click={backToTop}>
        expand_circle_up
    </span>
</main>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Inter&family=Libre+Baskerville&family=Playfair+Display:wght@600&display=swap");
    * {
        transition: background-color 0.5s ease-in;
    }

    :root {
        --bgHue: 180;
        --bgSaturation: 30%;
        --bgLightness: 50%;
        --mainColor: hsl(var(--bgHue), var(--bgSaturation), var(--bgLightness));
        --secondaryColor: hsl(
            calc(var(--bgHue) + 90),
            var(--bgSaturation),
            var(--bgLightness)
        );
    }

    .section {
        position: relative;
        display: flex;
        flex-direction: column;
    }

    #section1 {
        position: relative;
        margin: auto;
        text-align: center;
        display: flex;
        height: 100svh;
        background-color: hsl(
            var(--bgHue),
            var(--bgSaturation),
            var(--bgLightness)
        );
        flex-direction: row;
    }

    #section2 {
        position: relative;
        margin: auto;
        text-align: center;
        display: flex;
        height: 75svh;
        background-color: hsl(
            calc(var(--bgHue) + 15),
            var(--bgSaturation),
            var(--bgLightness)
        );
    }

    #section3 {
        position: relative;
        margin: auto;
        text-align: center;
        display: flex;
        height: 75svh;
        background-color: hsl(
            calc(var(--bgHue) + 200),
            var(--bgSaturation),
            var(--bgLightness)
        );
    }

    #section4 {
        position: relative;
        margin: auto;
        text-align: center;
        display: flex;
        height: 75svh;
        background-color: hsl(
            calc(var(--bgHue) + 225),
            var(--bgSaturation),
            var(--bgLightness)
        );
    }

    .card {
        z-index: 5;
        position: absolute;
        top: 50%;
        transform: translateY(-50%) !important;
        display: flex;
        flex-direction: column;
        text-align: center;
        width: 50em;
        height: auto;
        padding: 1.5rem;
        background: rgba(255, 255, 255, 0.2);
        box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
        backdrop-filter: blur(15.5px);
        -webkit-backdrop-filter: blur(15.5px);
        border-radius: 10px;
        border: 1px solid rgba(255, 255, 255, 0.18);
    }

    @keyframes hover {
        0% {
            transform: translateY(-5px);
        }
        25% {
            transform: translateY(-10px);
        }
        50% {
            transform: translateY(-15px);
        }
        75% {
            transform: translateY(-10px);
        }
        100% {
            transform: translateY(-5px);
        }
    }

    #primary {
        margin-left: 10rem;
        /* background-color: hsla(
            calc(var(--bgHue) + 90),
            var(--bgSaturation),
            var(--bgLightness),
            20%
        ); */
        border: 1px solid var(--secondaryColor);
    }

    #secondary {
        position: absolute;
        right: 0;
        margin-right: 10rem;
        /* background-color: hsla(
            calc(var(--bgHue) + 180),
            var(--bgSaturation),
            var(--bgLightness),
            20%
        ); */
        border: 1px solid var(--mainColor);
    }

    .topwave {
        z-index: 2;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        overflow: hidden;
        line-height: 0;
    }

    .topwave svg {
        position: relative;
        display: block;
        width: calc(300% + 1.3px);
        height: 196px;
    }

    .topwave .shape-fill {
        fill: #ffffff22;
    }

    .bottomwave {
        z-index: 2;
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        overflow: hidden;
        line-height: 0;
        transform: rotate(180deg);
    }

    .bottomwave svg {
        position: relative;
        display: block;
        width: calc(300% + 1.3px);
        height: 361px;
    }

    .bottomwave .shape-fill {
        fill: #ffffff22;
    }

    .header {
        color: white;
        position: relative;
        font-size: 2.5rem;
        font-family: "Playfair Display", serif;
        margin: 0;
        font-stretch: 110%;
    }

    .header::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        height: 1px;
        background-image: linear-gradient(to right, #ffffff, #797979);
    }

    .subheader {
        top: 1.5rem;
        color: white;
        position: relative;
        font-size: 1.5rem;
        font-family: "Inter", sans-serif;
        font-stretch: 110%;
        margin-bottom: 2rem;
    }

    .subheader::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        height: 1px;
        background-image: linear-gradient(to right, #77777760, #ffffff07);
    }

    .content {
        color: white;
        margin: 0;
        font-family: "Inter", sans-serif;
        font-size: 1rem;
        margin: 1rem 0rem;
    }

    .emphasized {
        font-weight: bold;
        font-size: 1.5rem;
    }

    .imagecontent {
        margin: 1rem 1rem;
        display: flex;
        flex-direction: row;
        gap: 7rem;
    }

    .portrait {
        height: 150px;
        width: 3rem;
        scale: 35%;
        transition: all 0.5s ease-in-out;
    }

    img {
        z-index: -1;
    }

    img:hover {
        filter: brightness(120%);
        cursor: pointer;
        animation: hover 0.5s ease-in-out infinite;
        transition: all 0.5s ease-in-out;
    }

    #topbutton {
        font-variation-settings: "FILL" 0, "wght" 400, "GRAD" 0, "opsz" 24;
        position: fixed;
        bottom: 1rem;
        left: 1rem;
        font-size: 50px;
        color: white;
        user-select: none;
        transition: all 0.2s linear;
    }

    #topbutton:hover {
        transition: all 0.2s linear;
        color: #919191;
        cursor: pointer;
    }

    .material-symbols-outlined {
        font-variation-settings: "FILL" 0, "wght" 400, "GRAD" 0, "opsz" 24;
    }

    #image1 {
        position: static;
        width: auto;
        height: 31px;
    }

    #container {
        display: flex;
        flex-direction: row;
        height: 300px;
    }

    #dirt {
        display: flex;
        flex-direction: column;
        color: white;
        text-align: center;
        flex: auto;
        align-items: center;
    }

    #stone {
        display: flex;
        flex-direction: column;
        color: white;
        text-align: center;
        flex: auto;
        border-left: 1px solid #b9b9b9;
        border-top: none;
        border-right: 1px solid #b9b9b9;
        border-bottom: none;
        align-items: center;
    }

    #diamond {
        display: flex;
        flex-direction: column;
        color: white;
        text-align: center;
        flex: auto;
        align-items: center;
    }

    ul {
        list-style-type: square;
        line-height: 2.5rem;
    }

    .subscribeButton {
        width: 80px;
        text-align: center;
        border: 2px solid var(--mainColor);
        border-radius: 12px;
        background-color: rgba(202, 255, 202, 0.137);
        transition: all 0.3s ease-in-out;
    }

    .subscribeButton:hover {
        background-color: rgba(202, 255, 202, 0.562);
        transition: all 0.3s ease-in-out;
    }

    .subscribeButton:active {
        transform: translateY(5px);
        transition: all 0.3s ease-in-out;
    }
</style>
