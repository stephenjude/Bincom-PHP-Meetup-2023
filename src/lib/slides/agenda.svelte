<script lang="ts">
    import {Slide} from '@components'

    export let title: string;
    export let item1: string;
    export let item2: string;
    export let item3: string;

    export let item4: string;

    export let item5: string;

</script>

<Slide animate>
    <div class="text-left space-y-6">
        <h1 class="text-[4rem]">{title}</h1>
    </div>
</Slide>

<Slide animate>
    <div class="text-left space-y-6">
        <h1 class="text-[2rem]">{title}</h1>
        <li>{item1}</li>
    </div>
</Slide>

<Slide animate>
    <div class="text-left space-y-6">
        <h1 class="text-[2rem]">{title}</h1>
        <li>{item1}</li>
        <li>{item2}</li>
    </div>
</Slide>

<Slide animate>
    <div class="text-left space-y-6">
        <h1 class="text-[2rem]">{title}</h1>
        <li>{item1}</li>
        <li>{item2}</li>
        <li>{item3}</li>
    </div>
</Slide>

<Slide animate>
    <div class="text-left space-y-6">
        <h1 class="text-[2rem]">{title}</h1>
        <li>{item1}</li>
        <li>{item2}</li>
        <li>{item3}</li>
        <li>{item4}</li>
    </div>
</Slide>

<Slide animate>
    <div class="text-left space-y-6">
        <h1 class="text-[2rem]">{title}</h1>
        <li>{item1}</li>
        <li>{item2}</li>
        <li>{item3}</li>
        <li>{item4}</li>
        <li>{item5}</li>
    </div>
</Slide>
