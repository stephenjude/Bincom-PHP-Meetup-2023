<script lang="ts">
	import { Code, Slide} from '@components'
</script>

<Slide animate>
	<div class="text-left space-y-6">
		<h1 class="text-[2rem]">Laravel Example: Cross-Site Request Forgery (Secured ✅)</h1>
		<div class="w-[1020px]">
			<Code lang="php" lines="2|5">
				{`
<form method="POST" action="/profile">
    @csrf

    <!-- Equivalent to... -->
    <input type="hidden" name="_token" value="{{ csrf_token() }}" />
</form>
        	`}
			</Code>
		</div>
	</div>
</Slide>
