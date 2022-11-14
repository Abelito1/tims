<script>
	import admin from '$lib/images/Admin-Profile.png';
	import Sidebar from '$lib/components/Sidebar.svelte';
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
										EXECUTIVES
									</h1>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</main>
	<div class="bg-white">
		<div class="mx-auto py-12 px-4 max-w-7xl sm:px-6 lg:px-8 lg:py-24">
			<div class="grid grid-cols-1 gap-12 lg:grid-cols-3 lg:gap-8">
				<div class="space-y-5 sm:space-y-4">
					<h2 class="text-3xl font-extrabold tracking-tight sm:text-4xl">Meet our leadership</h2>
					<p class="text-xl text-gray-500 text-justify">
						Inopacan Hindang Hilongos Transportation COOPERATIVE (INHITRANSCO), It’s a organization
						that do transportation from Inopacan to Bato. First grand launching of modern PUVs in
						Inopacan Baywalk, Inopacan Leyte , Febuary 4, 2022. Inopacan to Bato V.V bus has finally
						arrived last January 27,2022, 13 units for now.
					</p>
				</div>
				<div class="lg:col-span-2">
					<ul
						role="list"
						class="space-y-12 sm:grid sm:grid-cols-2 sm:gap-12 sm:space-y-0 lg:gap-x-8"
					>
						<li>
							<div class="flex items-center space-x-4 lg:space-x-6">
								<img class="w-16 h-16 rounded-full lg:w-20 lg:h-20" src={admin} alt="" />
								<div class="font-medium text-lg leading-6 space-y-1">
									<h3>Leslie Alexander</h3>
									<p class="text-indigo-600">Co-Founder / CEO</p>
								</div>
							</div>
						</li>

						<!-- More people... -->
					</ul>
				</div>
			</div>
		</div>
	</div>
</div>
