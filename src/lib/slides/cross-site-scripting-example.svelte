<script lang="ts">
	import { Code, Slide} from '@components'
</script>

<Slide animate>
	<div class="text-left space-y-6">
		<h1 class="text-[2rem]">PHP Example: Cross-Site Scripting (Malicious ❌)</h1>
		<div class="w-[1020px]">
			<Code lang="php" lines="3|1|5">
				{`
$input = $_GET('fullname'); //"<script>alert('Hack');</script>";

echo "Hello $input, you are welcome";

// Output: Hello <script>alert('Hack');</script>, you are welcome
        	`}
			</Code>
		</div>
	</div>
</Slide>

<Slide animate>
	<div class="text-left space-y-6">
		<h1 class="text-[2rem]">PHP Example: Cross-Site Scripting (Secured ✅)</h1>

		<div class="w-[1020px]">
			<Code lang="php" lines="3|7">
				{`
$input = $_GET('fullname'); //"<script>alert('Hack');</script>";

$sanitizedInput = htmlspecialchars($input);

echo "Hello $sanitizedInput, you are welcome";

// Output: Hello &lt;script&gt;alert(&#039;Hack&#039;);&lt;/script&gt;, you are welcome
        	`}
			</Code>
		</div>
	</div>
</Slide>

<Slide animate>
	<div class="text-left space-y-6">
		<h1 class="text-[2rem]">Laravel Example: Cross-Site Scripting (Malicious ❌)</h1>
		<div class="w-[1020px]">
			<Code lang="php" lines="3|1|5">
				{`
@php($input = $_GET('fullanme')); // "<script>alert('Hack');</script>";

{!! $input !!}

// Output: <script>alert('Hack');</script>
`}
			</Code>
		</div>
	</div>
</Slide>

<Slide animate>
	<div class="text-left space-y-6">
		<h1 class="text-[2rem]">Laravel Example: Cross-Site Scripting (Secured ✅)</h1>
		<div class="w-[1020px]">
			<Code lang="php" lines="3|5">
				{`
@php($input = "<script>alert('Hack');</script>");

{{ $input }}

// Output: &lt;script&gt;alert(&#039;Hack&#039;);&lt;/script&gt;
        	`}
			</Code>
		</div>
	</div>
</Slide>
