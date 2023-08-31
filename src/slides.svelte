<script lang="ts">
    import {Code, Presentation, Slide} from '@components'
    import {About, OneSlot, Quote, SqlInjectionExample, CrossSiteScriptingExample, CrossSiteRequestForgryExample, Thanks, Title,} from '@lib/slides'

    let title: string = 'Securing Web Applications'
    let subtitle: string = 'PHP & Laravel Applications'
    let author: string = 'Stephen Jude'
    let event: string = 'Bincom PHP Meetup'
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
            event={event}
    />

    <About
            author={author}
            role={role}
            company={company}
            github={github}
            x={x}
            avatar={avatar}
    />

    <OneSlot
            title="PHP Usage Statistics ">
        <ul class="list-disc p-4">
            <li class="leading-loose">Powers over 80% of the web. 😇</li>
        </ul>
    </OneSlot>
    <OneSlot
            title="Malicious Traffic Statistics (2018)">
        <ul class="list-disc p-4">
            <li class="leading-normal">
                PHP was identified as the target of 81% of the web’s malicious traffic.😱
            </li>
        </ul>
    </OneSlot>

    <OneSlot
            title="Malicious Exploits Statistics (2018)">
        <ul class="list-disc p-4">
            <li class="leading-normal">
                PHP accounts for 68% of web's malicious exploits.😬
            </li>
        </ul>
    </OneSlot>

    <Quote
            avatar="https://londonspeakerbureau.com/wp-content/uploads/2017/04/Martina_Navratilova_Keynote_Speaker-300x300.jpg"
            author="Martina Navratilova"
            company="Former Wimbledon Champion"
            quote="Security used to be an inconvenience sometimes, but now it’s a necessity all the time.">
    </Quote>

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
            <span class="uppercase text-red-400 font-bold">inject and execute malicious code</span> into a web application to control and steal user's information.
        </h2>
    </OneSlot>

    <OneSlot
            title="Prevent Cross-Site Scripting (XSS) 👺">
        <li class="leading-normal">
            Always
            <span class="uppercase text-green-400 font-bold">Sanitze</span> input and output data.
        </li>
        <li class="leading-normal">
            Use <span class="uppercase text-green-400 font-bold"> Anti-XSS</span>
            libraries, template engines & frameworks.
        </li>
    </OneSlot>

    <CrossSiteScriptingExample/>

    <OneSlot
            title="Cross-Site Request Forgery (CSRF) 🤡 ?">
        <h2 class="leading-normal">
            Cross-site request forgery is a security vulnerability empowers attackers to
            <span class="uppercase text-red-400 font-bold">perform unauthorised commands</span> on behalf of an authenticated web application user.
        </h2>
    </OneSlot>

    <OneSlot
            title="Prevent Cross-Site Request Forgery (CSRF) 🤡">
        <li class="leading-normal">
            Use
            <span class="uppercase text-green-400 font-bold">authentication (CSRF)</span> token.
        </li>
        <li class="leading-normal">
            Use <span class="uppercase text-green-400 font-bold">CSRF</span>
            libraries, template engines & frameworks.
        </li>
    </OneSlot>

    <CrossSiteRequestForgryExample/>


    <Slide animate>
        <div class="text-left space-y-6">
            <h1 class="text-[4rem]">Advance Security Techniques</h1>
        </div>
    </Slide>

    <Thanks/>
</Presentation>
