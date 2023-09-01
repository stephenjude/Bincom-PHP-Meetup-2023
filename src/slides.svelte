<script lang="ts">
    import {Presentation, Slide} from '@components'
    import {
        About,
        Agenda,
        CrossSiteRequestForgryExample,
        CrossSiteScriptingExample,
        OneSlot,
        SqlInjectionExample,
        Thanks,
        Title,
        WhySecurity,
    } from '@lib/slides'

    let title: string = 'Stratagies For Securing Web Applications'
    let subtitle: string = 'PHP & Laravel Applications'
    let author: string = 'Stephen Jude'
    let event: string = '— Bincom PHP Meetup'
    let role: string = 'CTO'
    let company: string = 'Pay4Me App'
    let github: string = 'stephenjude'
    let x: string = 'stephenjude_'
    let avatar: string = 'https://github.com/stephenjude.png'
</script>

<Presentation>
    <Title
            title={title}
            subtitle={subtitle}
            author={author}
            event="{event}"
    />

    <About
            author={author}
            role={role}
            company={company}
            github={github}
            x={x}
            avatar={avatar}
    />

    <WhySecurity
            title="Why PHP Security ?"
            item1="Powers over 80% of the web 😇"
            item2="Target of 81% of malicious traffic 😱"
            item3="Accounts for 68% of malicious exploits 🥵">
    </WhySecurity>

    <Slide animate>
        <div class="w-full flex items-center justify-center">
            <img class="object-scale-down h-96 rounded-sm" src="img/with_great_power_comes_great_responsibility.jpg">
        </div>
    </Slide>

    <Agenda
            title="Agenda"
            item1="Common Security Threats."
            item2="Prevention Techniques."
            item3="Code Snippets & Examples (Laravel & PHP)"
            item4="Security Recommendations (Laravel & PHP)"
            item5="Question & Answers">
    </Agenda>

    <OneSlot
            title="PHP Security Threats (Top 3)">
        <ul class="list-disc p-4 leading-normal">
            <li>SQL Injection 👹</li>
            <li>Cross-Site Scripting (XSS) 👺</li>
            <li>Cross-site Request Forgery (CSRF) 🤡</li>
        </ul>
    </OneSlot>

    <OneSlot
            title="What is SQL Injection 👹 ?">
        <h2 class="leading-normal">
            SQL injection is a security vulnerability that empowers attackers to execute
            <span class="uppercase text-red-400 font-bold">unauthorized database operations</span>.
        </h2>
    </OneSlot>

    <OneSlot
            title="Prevent SQL Injection 👹">
        <h2 class="leading-normal">
            Use
            <span class="uppercase text-green-400 font-bold">prepared statements</span>.
        </h2>
    </OneSlot>

    <SqlInjectionExample/>

    <OneSlot
            title="What is Cross-Site Scripting (XSS) 👺 ?">
        <h2 class="leading-normal">
            Cross-site Scripting is a security vulnerability empowers attackers
            <span class="uppercase text-red-400 font-bold">inject and execute malicious code</span> into a web
            application to control and steal user's information.
        </h2>
    </OneSlot>

    <OneSlot
            title="Prevent Cross-Site Scripting (XSS) 👺">
        <li class="leading-normal">
            Always
            <span class="uppercase text-green-400 font-bold">Sanitze</span> input and output data.
        </li>
        <li class="leading-normal">
            Use <span class="uppercase text-green-400 font-bold"> Anti-XSS</span> supported
            libraries, template engines & frameworks.
        </li>
    </OneSlot>

    <CrossSiteScriptingExample/>

    <OneSlot
            title="Cross-Site Request Forgery (CSRF) 🤡 ?">
        <h2 class="leading-normal">
            Cross-site request forgery is a security vulnerability empowers attackers to
            <span class="uppercase text-red-400 font-bold">perform unauthorised commands</span> on behalf of an
            authenticated user.
        </h2>
    </OneSlot>

    <OneSlot
            title="Prevent Cross-Site Request Forgery (CSRF) 🤡">
        <li class="leading-normal">
            Use
            <span class="uppercase text-green-400 font-bold">authentication (CSRF)</span> token.
        </li>
        <li class="leading-normal">
            Use <span class="uppercase text-green-400 font-bold">CSRF</span> supported
            libraries, template engines & frameworks.
        </li>
    </OneSlot>

    <CrossSiteRequestForgryExample/>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[4rem]">Security Recomendations 🔥</h1>
        </div>
    </Slide>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[2rem]">Security Recomendations 🔥</h1>
            <li>Stack & infrastructure</li>
        </div>
    </Slide>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[2rem]">Security Recomendations 🔥</h1>
            <li>Stack & infrastructure ✅</li>
        </div>
    </Slide>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[2rem]">Security Recomendations 🔥</h1>
            <li>Stacks & infrastructure ✅</li>
            <li>HTTP security headers</li>
        </div>
    </Slide>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[2rem]">Security Recomendations 🔥</h1>
            <li>Stacks & infrastructure ✅</li>
            <li>HTTP security headers ✅</li>
        </div>
    </Slide>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[2rem]">Security Recomendations 🔥</h1>
            <li>Stacks & infrastructure ✅</li>
            <li>HTTP security headers ✅</li>
            <li>Validate your webhooks </li>
        </div>
    </Slide>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[2rem]">Security Recomendations 🔥</h1>
            <li>Stacks & infrastructure ✅</li>
            <li>HTTP security headers ✅</li>
            <li>Validate your webhooks ✅ </li>
        </div>
    </Slide>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[2rem]">Security Recomendations 🔥</h1>
            <li>Stacks & infrastructure ✅</li>
            <li>HTTP security headers ✅</li>
            <li>Validate your webhooks ✅</li>
            <li>Error tracking & monitoring</li>
        </div>
    </Slide>

    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[2rem]">Security Recomendations 🔥</h1>
            <li>Stacks & infrastructure ✅</li>
            <li>HTTP security headers ✅</li>
            <li>Validate your webhooks ✅</li>
            <li>Error tracking & monitoring ✅</li>
        </div>
    </Slide>

    <Thanks/>

</Presentation>
