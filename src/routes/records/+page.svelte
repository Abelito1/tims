<script>
	import Sidebar from '../_sidebar.svelte';
	import NavBar from '$lib/components/NavBar.svelte';

	let isClicked = false;

	function toggleDropdown() {
		isClicked = !isClicked;
	}
</script>

<Sidebar />
<div class="lg:pl-64 flex flex-col flex-1">
	<NavBar />
	<main class="flex-1 pb-8">
		<!-- Page header -->
		<div class="bg-white shadow">
			<div class="px-4 sm:px-6 lg:max-w-6xl lg:mx-auto lg:px-8">
				<div class="py-6 md:flex md:items-center md:justify-between lg:border-t lg:border-gray-200">
					<div class="flex-1 min-w-0">
						<!-- Profile -->
						<div class="flex items-center">
							<div>
								<div class="flex items-center">
									<img
										class="h-16 w-16 rounded-full sm:hidden"
										src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2.6&w=256&h=256&q=80"
										alt=""
									/>
									<h1
										class="ml-3 text-2xl font-bold leading-7 text-gray-900 sm:leading-9 sm:truncate"
									>
										RECORDS
									</h1>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</main>
</div>
