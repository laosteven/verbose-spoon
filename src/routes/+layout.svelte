<script lang="ts">
	import '../app.css';

	import { Toaster } from '$lib/components/ui/sonner';
	import { ModeWatcher } from 'mode-watcher';

	import ActivityTypeDialog from '../components/dialog/activity-type-dialog.svelte';
	import CalendarDialog from '../components/dialog/calendar-dialog.svelte';
	import StartDialog from '../components/dialog/start-dialog.svelte';
	import DrawerSettings from '../components/drawer/settings-drawer.svelte';
	import Sidebar from '../components/navigation/sidebar.svelte';
	import Topbar from '../components/navigation/topbar.svelte';
</script>

<!-- Global -->
<ModeWatcher />
<Toaster />

<!-- Overlays -->
<DrawerSettings />
<StartDialog />
<CalendarDialog />
<ActivityTypeDialog />

<!-- Navigation -->
<Sidebar />
<div class="grid h-screen w-full pl-[57px]">
	<div class="flex flex-col">
		<Topbar />
		<slot></slot>
	</div>
</div>
