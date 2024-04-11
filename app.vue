<script setup lang="ts">
const imgArray = [
    'assets/img/partners/daredata.svg',
    'assets/img/partners/PortoSpaceTeam.png',
    'assets/img/partners/feup.png',
    'assets/img/partners/gcloud.svg',
    'assets/img/partners/aptwind.png',
]
</script>

<template>
    <div class="main">
        <div class="hero">
            <div class="menu-bar">
                <div class="logo">
                    <img
                        alt="Inductiva.AI logo"
                        src="assets/img/inductiva-logo.svg"
                    />
                </div>
                <div class="menu-bar-items">
                    <a href="#features">Features</a>
                    <a href="#how">How it works</a>
                    <a href="#testimonials">Testimonials</a>
                    <a href="#faq">FAQs</a>
                </div>
                <div class="request-access">
                    <a>Request Access</a>
                </div>
            </div>
            <div class="welcome">
                <h1>Welcome to GENESYS</h1>
                <div class="copy">
                    <h5>
                        A call for remarkable students and outstanding
                        researchers. Join our early stage program. You will be
                        able to use our API for your educational projects
                    </h5>
                </div>
            </div>
        </div>
        <div class="intro section">
            <SectionHeader> Introducing our API</SectionHeader>
            <h2>
                Use Python to run your favorite simulator at scale, on the
                cloud.
            </h2>
            <div class="todo">
                Can we include a “programming black box”, a gif, editing a
                piece of code of simulation and running it? (similar to our blog
                “Programming at Inductiva)
            </div>
        </div>
        <div class="partners section">
            <h5>Partnered with the best Institutions</h5>
            <Vue3Marquee>
                <img src="assets/img/partners/daredata.svg" alt="DareData" width="300px" />
                <img src="assets/img/partners/PortoSpaceTeam.png" alt="Porto Space Team" width="300px" />
                <img src="assets/img/partners/gcloud.svg" alt="Google Cloud" width="300px" />
                <img src="assets/img/partners/feup.png" alt="FEUP" width="300px" />
                <img src="assets/img/partners/aptwind.png" alt="APTWIND" width="300px" />
            </Vue3Marquee>
        </div>
        <div id="features" class="what section">
            <SectionHeader> What you'll get</SectionHeader>
            <h2>Up to 1500 USD free credits for a month.</h2>
            <div class="feature-set">
                <FeatureCard>
                    <template #header-image>
                        <div class="todo"></div>
                    </template>
                    <template #title>
                        <a href="https://inductiva.ai/blog/article/5k-points-is-all-you-need">5K points is all you
                            need!</a>
                    </template>
                    description
                </FeatureCard>
                <FeatureCard>
                    <template #header-image>
                        <div class="todo"></div>
                    </template>
                    <template #title><a href="https://inductiva.ai/blog/article/api-synthetic-data-generation-1">Synthetic
                        Data for Physics-ML</a></template>
                    description
                </FeatureCard>
                <FeatureCard>
                    <template #header-image>
                        <div class="todo"></div>
                    </template>
                    <template #title><a
                        href="https://inductiva.ai/blog/article/scaling-coastal-engineering-projects-inductiva-api">Scaling
                        Coastal Engineering Projects</a>
                    </template>
                    description
                </FeatureCard>
            </div>
            <div class="feature-set badges">
                <Badge>Dedicated storage</Badge>
                <Badge>Run parallel simulations</Badge>
                <Badge>Setup MPI clusters</Badge>
                <Badge>Use last generation CPUs</Badge>
            </div>
        </div>
        <div id="how" class="how section">
            <SectionHeader> How it works</SectionHeader>
            <h2>Simple onboarding process.</h2>
            <div class="onboarding">
                <OnboardingStep>
                    <template #icon>
                        <div class="todo"></div>
                    </template>
                    <template #title>Login to Inductiva Console</template>
                    All you need is a Gmail account
                </OnboardingStep>
                <OnboardingStep>
                    <template #icon>
                        <div class="todo"></div>
                    </template>
                    <template #title>Install your API Key</template>
                    description
                </OnboardingStep>
                <OnboardingStep>
                    <template #icon>
                        <div class="todo"></div>
                    </template>
                    <template #title>Access the power</template>
                    Scale your simulations and change the world
                </OnboardingStep>
            </div>
        </div>
        <div id="testimonials" class="testimonials section">
            <SectionHeader> Testimonial</SectionHeader>
            <div class="todo" style="width: 640px; height: 480px">
                INTERVIEW WITH JOÃO
            </div>
        </div>
        <div class="stats section">
            <div class="items">
                <div>
                    <h1>11</h1>
                    <h5>Open Source Simulators</h5>
                    <h5>(and counting)</h5>
                </div>
                <div class="divider"></div>
                <div>
                    <h1>20+</h1>
                    <h5>Simulations in parallel</h5>
                </div>
                <div class="divider"></div>
                <div>
                    <h1>100+</h1>
                    <h5>Access to Virtual Machine Types</h5>
                </div>
            </div>
        </div>
        <div id="faq" class="faq section">
            <SectionHeader>FAQs</SectionHeader>
            <h2>We've got the answers</h2>
            <faq></faq>
            <span class="more">
                Still have more questions? Contact our help center.
            </span>
        </div>
        <div class="end section">
            <h2>Get ready to start changing the world.<br />One step at a time!</h2>
        </div>
        <div class="footer">
            <div class="items">
                <div>Contact</div>
                <div>Privacy & Cookie Policy</div>
                <div>Terms & Conditions</div>
                <div>Copyright 2024 Inductiva</div>
            </div>
        </div>
    </div>
</template>

<style>
@import url('/assets/css/styles.css');

.main {
    display: grid;
    grid-template-areas:
        'hero'
        'partners'
        'intro'
        'what'
        'how'
        'testimonials'
        'stats'
        'faq'
        'end'
        'footer';
    grid-template-columns: 1fr;
    grid-template-rows: 500px repeat(8, minmax(500px, auto)) 100px;
    width: 100%;
    background-color: var(--gen-bg-color);
    @media (max-width: 390px) {
        grid-template-rows: 400px repeat(8, minmax(400px, auto)) 50px;
    }
}

.hero {
    grid-area: hero;
    background-color: var(--ind-dark-int);
    color: var(--ind-full-white);
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    justify-items: center;
    align-items: center;
    background-image: linear-gradient(
        180deg,
        rgba(0, 1, 4, 0.37) 0%,
        var(--gen-bg-color) 100%
    ),
    url('assets/img/hero.webp');
    background-size: cover;
    background-position: 50% 50%;
    background-repeat: no-repeat;
    @media (max-width: 390px) {
        background-position: 80% 50%;
    }
}

.welcome {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 4rem;
    width: 100%;
}

.copy {
    display: flex;
    text-align: center;
    width: 40%;
    @media (max-width: 390px) {
        margin-top: 30px;
        width: 90%;
    }
}

h1 {
    font-size: 4rem;
    background: linear-gradient(to right, #888888 0%, #ffffff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    @media (max-width: 390px) {
        font-size: 3rem;
        line-height: 100%;
        text-align: center;
    }
}

h2 {
    max-width: 75%;
    font-size: 2.5rem;
    font-weight: lighter;
    text-align: center;
    margin-bottom: 40px;
    background: linear-gradient(to left, #444444 0%, #ffffff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    @media (max-width: 390px) {
        max-width: 100%;
        font-size: 2rem;
        line-height: 120%;
    }
}

h5 {
    font-size: 1rem;
    font-weight: lighter;
    color: var(--dark-text-color);
}

.menu-bar {
    display: flex;
    align-items: center;
    width: 80%;
    justify-content: space-between;
    padding: 10px;
    margin: 40px 0 70px 0;

    .logo {
        img {
            width: 170px;
        }
    }

    @media (max-width: 900px) and (min-width: 650px) {
        width: 100%;
    }

    .menu-bar-items {
        background-color: var(--nav-buttons-bg-color);
        border-color: var(--nav-buttons-bg-color);
        border-width: 1px;
        border-radius: 16px;
        padding: 10px;

        a {
            padding: 8px;
            color: var(--nav-buttons-color);
            text-decoration: none;
            background-color: var(--nav-buttons-bg-color);
        }

        @media (max-width: 650px) {
            display: none;
        }
    }

    .request-access {
        a {
            padding: 12px;
            color: var(--nav-buttons-color);
            text-decoration: none;
            font-weight: bolder;
            background-color: var(--ind-main-blue);
            border-color: var(--ind-main-blue);
            border-width: 1px;
            border-radius: 16px;
        }
    }
}

.section {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    justify-self: center;
    width: 90%;
}

.partners {
    grid-area: partners;
    display: flex;
    align-items: center;
    padding-top: 20px;

    .marquee {
        max-width: 75%;
    }

    .card {
        display: flex;
        justify-content: center;
        min-width: 150px;
        margin-right: 50px;
    }
}

.intro {
    grid-area: intro;
}

.what {
    grid-area: what;
}

.how {
    grid-area: how;
}

.testimonials {
    grid-area: testimonials;
}

.stats {
    grid-area: stats;

    .items {
        display: flex;
        width: 50%;
        justify-content: space-between;
        @media (max-width: 390px) {
            flex-wrap: wrap;
            flex-direction: column;
            gap: var(--gap);
            width: 100%;
        }

        .divider {
            background-image: linear-gradient(
                180deg,
                var(--gen-bg-color),
                #333333,
                var(--gen-bg-color)
            );
            min-width: 3px;
            @media (max-width: 390px) {
                display: none;
            }
        }

        > div {
            text-align: center;
        }
    }
}

.end {
    grid-area: end;
}

.faq {
    grid-area: faq;
    width: 65%;
    @media (max-width: 390px) {
        width: 90%;
    }

    .more {
        margin-top: 30px;
        font-size: 0.8rem;
    }
}

.feature-set {
    display: flex;
    gap: var(--gap);
    @media (max-width: 390px) {
        flex-wrap: wrap;
    }

    &.badges {
        display: flex;
        flex-wrap: wrap;
        margin-top: 40px;
        gap: var(--gap);
    }
}

.onboarding {
    gap: var(--gap);
    display: flex;
    @media (max-width: 390px) {
        flex-wrap: wrap;
    }
}

.footer {
    grid-area: footer;
    display: flex;
    justify-content: center;
    margin-top: 80px;
    padding-bottom: 40px;

    .items {
        display: flex;
        justify-content: space-between;
        width: 70%;
    }
}

.todo {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: var(--gap);
    margin: var(--gap);
    background-color: #ff475744;
    background-image: linear-gradient(1turn, var(--table-bg-color), #00000099, var(--table-bg-color)), url("assets/img/placeholder.svg");
    color: white;
    font-size: 1.5rem;
    font-weight: bolder;
    min-width: 100px;
    min-height: 100px;
}

a:visited, a:link {
    color: var(--link-color)
}

a:hover {
    color: var(--link-hover-color)
}
</style>
