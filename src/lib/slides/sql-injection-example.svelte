<script lang="ts">
	import { Code, Slide} from '@components'
</script>

<Slide animate>
	<div class="text-left space-y-6">
		<h1 class="text-[4rem]">PHP Example: SQL Injection</h1>
	</div>
</Slide>

<Slide animate>
	<div class="text-left space-y-6">
		<h1 class="text-[2rem]">PHP Example: SQL Injection (Malicious ❌)</h1>
		<div class="w-[1020px]">
			<Code lang="php" lines="3|1|5">
				{`
            $id = "1; DROP TABLE users;";

            $statement = "SELECT * FROM users where id = $id";

           // Output: SELECT * FROM users where id=1; DROP TABLE users;
        	`}
			</Code>
		</div>
	</div>
</Slide>

<Slide animate>
	<div class="text-left space-y-6">
		<h1 class="text-[2rem]">PHP Example: SQL Injection (Secured ✅)</h1>
		<div class="w-[1020px]">
			<Code lang="php" lines="3|1|5-7|9|11">
				{`
				$id = "1; DROP TABLE users;";

				$statement = $database->prepare("SELECT * FROM users where id = ?");

				$statement->bind_param('s', $id); // MySQLi: bind parameter

				$statement->execute(); // MySQLi: bind parameter

				$statement->execute([$id]); // PDO: bind parameter & execute query

				// Output: SELECT * FROM users where id="1; DROP TABLE users";
        	`}
			</Code>
		</div>
	</div>
</Slide>
