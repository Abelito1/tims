<script>
	let isClicked = false;

	function toggleDropdown() {
		isClicked = !isClicked;
	}
	import admin from '$lib/images/Admin-Profile.png';
	import Sidebar from '../_sidebar.svelte';
	import NavBar from '$lib/components/NavBar.svelte';
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
							<img class="hidden h-16 w-16 rounded-full sm:block" src={admin} alt="" />
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
										Welcome!
									</h1>
								</div>
								<dl class="mt-6 flex flex-col sm:ml-3 sm:mt-1 sm:flex-row sm:flex-wrap">
									<dt class="sr-only">Company</dt>
									<dd
										class="flex items-center text-sm text-gray-500 font-medium capitalize sm:mr-6"
									>
										<!-- Heroicon name: solid/office-building -->
										<svg
											class="flex-shrink-0 mr-1.5 h-5 w-5 text-gray-400"
											xmlns="http://www.w3.org/2000/svg"
											viewBox="0 0 20 20"
											fill="currentColor"
											aria-hidden="true"
										>
											<path
												fill-rule="evenodd"
												d="M4 4a2 2 0 012-2h8a2 2 0 012 2v12a1 1 0 110 2h-3a1 1 0 01-1-1v-2a1 1 0 00-1-1H9a1 1 0 00-1 1v2a1 1 0 01-1 1H4a1 1 0 110-2V4zm3 1h2v2H7V5zm2 4H7v2h2V9zm2-4h2v2h-2V5zm2 4h-2v2h2V9z"
												clip-rule="evenodd"
											/>
										</svg>
										INHITRANSCO
									</dd>
									<dt class="sr-only">Account status</dt>
									<dd
										class="mt-3 flex items-center text-sm text-gray-500 font-medium sm:mr-6 sm:mt-0 capitalize"
									>
										<!-- Heroicon name: solid/check-circle -->
										<svg
											class="flex-shrink-0 mr-1.5 h-5 w-5 text-green-400"
											xmlns="http://www.w3.org/2000/svg"
											viewBox="0 0 20 20"
											fill="currentColor"
											aria-hidden="true"
										>
											<path
												fill-rule="evenodd"
												d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
												clip-rule="evenodd"
											/>
										</svg>
										Verified account
									</dd>
								</dl>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</main>
	<div class="px-4 mt-6 sm:px-6 lg:px-8">
		<h2 class="text-gray-500 text-xs font-medium uppercase tracking-wide">Pinned</h2>
		<ul role="list" class="grid grid-cols-1 gap-4 sm:gap-6 sm:grid-cols-2 xl:grid-cols-4 mt-3">
			<li class="relative col-span-1 flex shadow-sm rounded-md">
				<div
					class="flex-shrink-0 flex items-center justify-center w-16 bg-pink-600 text-white text-sm font-medium rounded-l-md"
				>
					IT
				</div>
				<div
					class="flex-1 flex items-center justify-between border-t border-r border-b border-gray-200 bg-white rounded-r-md truncate"
				>
					<div class="flex-1 px-4 py-2 text-sm truncate">
						<a href="/inhitransco" class="text-gray-900 font-medium hover:text-gray-600">
							INHITRANSCO
						</a>
						<p class="text-gray-500">1 Member</p>
					</div>
					<div class="flex-shrink-0 pr-2">
						<button
							type="button"
							class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-purple-500"
							id="pinned-project-options-menu-0-button"
							aria-expanded="false"
							aria-haspopup="true"
						>
							<span class="sr-only">Open options</span>
							<!-- Heroicon name: solid/dots-vertical -->
							<svg
								class="w-5 h-5"
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true"
							>
								<path
									d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
								/>
							</svg>
						</button>

						<!--
					  Dropdown menu, show/hide based on menu state.
	
					  Entering: "transition ease-out duration-100"
						From: "transform opacity-0 scale-95"
						To: "transform opacity-100 scale-100"
					  Leaving: "transition ease-in duration-75"
						From: "transform opacity-100 scale-100"
						To: "transform opacity-0 scale-95"
					-->
						<div
							class="z-10 mx-3 origin-top-right absolute right-10 top-3 w-48 mt-1 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 divide-y divide-gray-200 focus:outline-none hidden"
							role="menu"
							aria-orientation="vertical"
							aria-labelledby="pinned-project-options-menu-0-button"
							tabindex="-1"
						>
							<div class="py-1" role="none">
								<!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-0">View</a
								>
							</div>
							<div class="py-1" role="none">
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-1">Removed from pinned</a
								>
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-2">Share</a
								>
							</div>
						</div>
					</div>
				</div>
			</li>

			<!-- More items... -->
		</ul>
	</div>
	<div class="px-4 mt-6 sm:px-6 lg:px-8">
		<ul role="list" class="grid grid-cols-1 gap-4 sm:gap-6 sm:grid-cols-2 xl:grid-cols-4 mt-3">
			<li class="relative col-span-1 flex shadow-sm rounded-md">
				<div
					class="flex-shrink-0 flex items-center justify-center w-16 bg-blue-600 text-white text-sm font-medium rounded-l-md"
				>
					AP
				</div>
				<div
					class="flex-1 flex items-center justify-between border-t border-r border-b border-gray-200 bg-white rounded-r-md truncate"
				>
					<div class="flex-1 px-4 py-2 text-sm truncate">
						<a href="/applicant" class="text-gray-900 font-medium hover:text-gray-600">
							APPLICANT REQUEST
						</a>
						<p class="text-gray-500">1 request</p>
					</div>
					<div class="flex-shrink-0 pr-2">
						<button
							type="button"
							class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-purple-500"
							id="pinned-project-options-menu-0-button"
							aria-expanded="false"
							aria-haspopup="true"
						>
							<span class="sr-only">Open options</span>
							<!-- Heroicon name: solid/dots-vertical -->
							<svg
								class="w-5 h-5"
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true"
							>
								<path
									d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
								/>
							</svg>
						</button>

						<!--
					  Dropdown menu, show/hide based on menu state.
	
					  Entering: "transition ease-out duration-100"
						From: "transform opacity-0 scale-95"
						To: "transform opacity-100 scale-100"
					  Leaving: "transition ease-in duration-75"
						From: "transform opacity-100 scale-100"
						To: "transform opacity-0 scale-95"
					-->
						<div
							class="z-10 mx-3 origin-top-right absolute right-10 top-3 w-48 mt-1 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 divide-y divide-gray-200 focus:outline-none hidden"
							role="menu"
							aria-orientation="vertical"
							aria-labelledby="pinned-project-options-menu-0-button"
							tabindex="-1"
						>
							<div class="py-1" role="none">
								<!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-0">View</a
								>
							</div>
							<div class="py-1" role="none">
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-1">Removed from pinned</a
								>
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-2">Share</a
								>
							</div>
						</div>
					</div>
				</div>
			</li>

			<!-- More items... -->
		</ul>
	</div>
	<div class="px-4 mt-6 sm:px-6 lg:px-8">
		<ul role="list" class="grid grid-cols-1 gap-4 sm:gap-6 sm:grid-cols-2 xl:grid-cols-4 mt-3">
			<li class="relative col-span-1 flex shadow-sm rounded-md">
				<div
					class="flex-shrink-0 flex items-center justify-center w-16 bg-green-600 text-white text-sm font-medium rounded-l-md"
				>
					RC
				</div>
				<div
					class="flex-1 flex items-center justify-between border-t border-r border-b border-gray-200 bg-white rounded-r-md truncate"
				>
					<div class="flex-1 px-4 py-2 text-sm truncate">
						<a href="/records" class="text-gray-900 font-medium hover:text-gray-600"> RECORDS </a>
						<p class="text-gray-500">0 File</p>
					</div>
					<div class="flex-shrink-0 pr-2">
						<button
							type="button"
							class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-purple-500"
							id="pinned-project-options-menu-0-button"
							aria-expanded="false"
							aria-haspopup="true"
						>
							<span class="sr-only">Open options</span>
							<!-- Heroicon name: solid/dots-vertical -->
							<svg
								class="w-5 h-5"
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true"
							>
								<path
									d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
								/>
							</svg>
						</button>

						<!--
					  Dropdown menu, show/hide based on menu state.
	
					  Entering: "transition ease-out duration-100"
						From: "transform opacity-0 scale-95"
						To: "transform opacity-100 scale-100"
					  Leaving: "transition ease-in duration-75"
						From: "transform opacity-100 scale-100"
						To: "transform opacity-0 scale-95"
					-->
						<div
							class="z-10 mx-3 origin-top-right absolute right-10 top-3 w-48 mt-1 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 divide-y divide-gray-200 focus:outline-none hidden"
							role="menu"
							aria-orientation="vertical"
							aria-labelledby="pinned-project-options-menu-0-button"
							tabindex="-1"
						>
							<div class="py-1" role="none">
								<!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-0">View</a
								>
							</div>
							<div class="py-1" role="none">
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-1">Removed from pinned</a
								>
								<a
									href="#"
									class="text-gray-700 block px-4 py-2 text-sm"
									role="menuitem"
									tabindex="-1"
									id="pinned-project-options-menu-0-item-2">Share</a
								>
							</div>
						</div>
					</div>
				</div>
			</li>

			<!-- More items... -->
		</ul>
	</div>
</div>
