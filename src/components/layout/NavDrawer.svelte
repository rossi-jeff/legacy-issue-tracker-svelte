<script>
	import Drawer, { Content, Header, Title, Subtitle } from '@smui/drawer';
	import List, { Item, Text, Graphic } from '@smui/list';
	export /**
	 * @type {boolean | undefined}
	 */
	let open;
	export let navigate = () => {};
</script>

<Drawer variant="modal" fixed={false} bind:open style="z-index: 9999999">
	<Header>
		<Title>Issue Tracker</Title>
		<Subtitle>Built by Jeff Rossi</Subtitle>
	</Header>
	<Content>
		<List>
			<Item href="/" on:click={navigate}>
				<Graphic class="material-icons" aria-hidden="true">home</Graphic>
				<Text>Home</Text>
			</Item>
			<Item href="/dashboard" on:click={navigate}>
				<Graphic class="material-icons" aria-hidden="true">dashboard</Graphic>
				<Text>Dashboard</Text>
			</Item>
			<Item href="/projects" on:click={navigate}>
				<Graphic class="material-icons" aria-hidden="true">construction</Graphic>
				<Text>Projects</Text>
			</Item>
			<Item href="/issues" on:click={navigate}>
				<Graphic class="material-icons" aria-hidden="true">list</Graphic>
				<Text>Issues</Text>
			</Item>
			<Item href="/users" on:click={navigate}>
				<Graphic class="material-icons" aria-hidden="true">people</Graphic>
				<Text>Users</Text>
			</Item>
			<Item href="/timeclocks" on:click={navigate}>
				<Graphic class="material-icons" aria-hidden="true">punch_clock</Graphic>
				<Text>Time Clocks</Text>
			</Item>
		</List>
	</Content>
</Drawer>
