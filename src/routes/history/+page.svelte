<script>
	let isClicked = false;

	function toggleDropdown() {
		isClicked = !isClicked;
	}
	import admin from '$lib/images/Admin-Profile.png';
	import logo from '$lib/images/timslogo.png';
</script>

<div class="min-h-full">
	<!-- Off-canvas menu for mobile, show/hide based on off-canvas menu state. -->
	<div class="fixed inset-0 flex z-40 lg:hidden" role="dialog" aria-modal="true">
		<!--
        Off-canvas menu overlay, show/hide based on off-canvas menu state.
  
        Entering: "transition-opacity ease-linear duration-300"
          From: "opacity-0"
          To: "opacity-100"
        Leaving: "transition-opacity ease-linear duration-300"
          From: "opacity-100"
          To: "opacity-0"
      -->
		<div class="fixed inset-0 bg-gray-600 bg-opacity-75" aria-hidden="true" />

		<!--
        Off-canvas menu, show/hide based on off-canvas menu state.
  
        Entering: "transition ease-in-out duration-300 transform"
          From: "-translate-x-full"
          To: "translate-x-0"
        Leaving: "transition ease-in-out duration-300 transform"
          From: "translate-x-0"
          To: "-translate-x-full"
      -->
		<div class="relative flex-1 flex flex-col max-w-xs w-full pt-5 pb-4 bg-cyan-600">
			<!--
          Close button, show/hide based on off-canvas menu state.
  
          Entering: "ease-in-out duration-300"
            From: "opacity-0"
            To: "opacity-100"
          Leaving: "ease-in-out duration-300"
            From: "opacity-100"
            To: "opacity-0"
        -->
			<div class="absolute top-0 right-0 -mr-12 pt-2">
				<button
					type="button"
					class="ml-1 flex items-center justify-center h-10 w-10 rounded-full focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
				>
					<span class="sr-only">Close sidebar</span>
					<!-- Heroicon name: outline/x -->
					<svg
						class="h-6 w-6 text-white"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M6 18L18 6M6 6l12 12"
						/>
					</svg>
				</button>
			</div>

			<div class="flex-shrink-0 flex items-center px-4">
				<img
					class="h-8 w-auto"
					src="https://tailwindui.com/img/logos/easywire-logo-cyan-300-mark-white-text.svg"
					alt="Easywire logo"
				/>
			</div>
			<nav class="mt-5 flex-shrink-0 h-full divide-y  overflow-y-auto" aria-label="Sidebar">
				<div class="px-2 space-y-1">
					<!-- Current: "bg-cyan-800 text-white", Default: "text-cyan-100 hover:text-white hover:bg-cyan-600" -->
					<a
						href="#"
						class="bg-indigo-600 text-white group flex items-center px-2 py-2 text-base font-medium rounded-md"
						aria-current="page"
					>
						<!-- Heroicon name: outline/home -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
							/>
						</svg>
						Home
					</a>

					<a
						href="/history"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-base font-medium rounded-md"
					>
						<!-- Heroicon name: outline/clock -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
							/>
						</svg>
						Calendar
					</a>

					<a
						href="#"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-base font-medium rounded-md"
					>
						<!-- Heroicon name: outline/scale -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M3 6l3 1m0 0l-3 9a5.002 5.002 0 006.001 0M6 7l3 9M6 7l6-2m6 2l3-1m-3 1l-3 9a5.002 5.002 0 006.001 0M18 7l3 9m-3-9l-6-2m0-2v2m0 16V5m0 16H9m3 0h3"
							/>
						</svg>
						Balances
					</a>

					<a
						href="#"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-base font-medium rounded-md"
					>
						<!-- Heroicon name: outline/credit-card -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"
							/>
						</svg>
						Cards
					</a>

					<a
						href="#"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-base font-medium rounded-md"
					>
						<!-- Heroicon name: outline/user-group -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"
							/>
						</svg>
						Recipients
					</a>

					<a
						href="#"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-base font-medium rounded-md"
					>
						<!-- Heroicon name: outline/document-report -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M9 17v-2m3 2v-4m3 4v-6m2 10H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"
							/>
						</svg>
						Reports
					</a>
				</div>
				<div class="mt-6 pt-6">
					<div class="px-2 space-y-1">
						<a
							href="#"
							class="group flex items-center px-2 py-2 text-base font-medium rounded-md text-cyan-100 hover:text-white hover:bg-cyan-600"
						>
							<!-- Heroicon name: outline/cog -->
							<svg
								class="mr-4 h-6 w-6 text-cyan-200"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								aria-hidden="true"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"
								/>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
								/>
							</svg>
							Settings
						</a>

						<a
							href="#"
							class="group flex items-center px-2 py-2 text-base font-medium rounded-md text-cyan-100 hover:text-white hover:bg-cyan-600"
						>
							<!-- Heroicon name: outline/question-mark-circle -->
							<svg
								class="mr-4 h-6 w-6 text-cyan-200"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								aria-hidden="true"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
								/>
							</svg>
							Help
						</a>

						<a
							href="#"
							class="group flex items-center px-2 py-2 text-base font-medium rounded-md text-cyan-100 hover:text-white hover:bg-cyan-600"
						>
							<!-- Heroicon name: outline/shield-check -->
							<svg
								class="mr-4 h-6 w-6 text-cyan-200"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								aria-hidden="true"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
								/>
							</svg>
							Privacy
						</a>
					</div>
				</div>
			</nav>
		</div>

		<div class="flex-shrink-0 w-14" aria-hidden="true">
			<!-- Dummy element to force sidebar to shrink to fit close icon -->
		</div>
	</div>

	<!-- Static sidebar for desktop -->
	<div class="hidden lg:flex lg:w-64 lg:flex-col lg:fixed lg:inset-y-0">
		<!-- Sidebar component, swap this element with another sidebar if you like -->
		<div class="flex flex-col flex-grow bg-gray-600 pt-5 pb-4 overflow-y-auto">
			<div class="flex items-center flex-shrink-0 px-4">
				<img class="h-24 w-auto mx-auto" src={logo} alt="Easywire logo" />
			</div>
			<nav
				class="mt-5 flex-1 flex flex-col divide-y divide-cyan-600 overflow-y-auto"
				aria-label="Sidebar"
			>
				<div class="px-2 space-y-1">
					<!-- Current: "bg-cyan-800 text-white", Default: "text-cyan-100 hover:text-white hover:bg-cyan-600" -->
					<a
						href="/dashboard"
						class="bg-cyan-800 text-white group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md"
						aria-current="page"
					>
						<!-- Heroicon name: outline/home -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
							/>
						</svg>
						Home
					</a>

					<a
						href="/history"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md"
					>
						<!-- Heroicon name: outline/clock -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
							/>
						</svg>
						Calendar
					</a>

					<a
						href="#"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md"
					>
						<!-- Heroicon name: outline/scale -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path fill="currentColor" d="M4 9h4v2H4V9z" /><path
								fill="currentColor"
								d="M16 2h-1V0H5v2H3v1.25L2.4 4H1v1.75L0 7v9h12l4-5V2zM2 5h8v2H2V5zm9 10H1V8h10v7zm1-8h-1V4H4V3h8v4zm2-2.5l-1 1.25V2H6V1h8v3.5z"
							/>
						</svg>
						Records
					</a>

					<a
						href="#"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md"
					>
						<!-- Heroicon name: outline/credit-card -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"
							/>
						</svg>
						Cards
					</a>

					<a
						href="#"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md"
					>
						<!-- Heroicon name: outline/user-group -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path fill="currentColor" d="M4 4h16v6H4zm0 9h16v2H4z" opacity=".3" /><path
								fill="currentColor"
								d="M20 2H4c-1.11 0-2 .89-2 2v11c0 1.11.89 2 2 2h4v5l4-2l4 2v-5h4c1.11 0 2-.89 2-2V4c0-1.11-.89-2-2-2zm0 13H4v-2h16v2zm0-5H4V4h16v6z"
							/>
						</svg>

						Members
					</a>

					<a
						href="#"
						class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md"
					>
						<!-- Heroicon name: outline/document-report -->
						<svg
							class="mr-4 flex-shrink-0 h-6 w-6 text-cyan-200"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								fill="currentColor"
								d="M15.73 3H8.27L3 8.27v7.46L8.27 21h7.46L21 15.73V8.27L15.73 3zM12 17.3c-.72 0-1.3-.58-1.3-1.3c0-.72.58-1.3 1.3-1.3c.72 0 1.3.58 1.3 1.3c0 .72-.58 1.3-1.3 1.3zm1-4.3h-2V7h2v6z"
							/>
						</svg>
						Reports
					</a>
				</div>
				<div class="mt-6 pt-6">
					<div class="px-2 space-y-1">
						<a
							href="#"
							class="group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md text-cyan-100 hover:text-white hover:bg-cyan-600"
						>
							<!-- Heroicon name: outline/cog -->
							<svg
								class="mr-4 h-6 w-6 text-cyan-200"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								aria-hidden="true"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"
								/>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
								/>
							</svg>
							Settings
						</a>

						<a
							href="#"
							class="group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md text-cyan-100 hover:text-white hover:bg-cyan-600"
						>
							<!-- Heroicon name: outline/question-mark-circle -->
							<svg
								class="mr-4 h-6 w-6 text-cyan-200"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								aria-hidden="true"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
								/>
							</svg>
							Help
						</a>

						<a
							href="#"
							class="group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md text-cyan-100 hover:text-white hover:bg-cyan-600"
						>
							<!-- Heroicon name: outline/shield-check -->
							<svg
								class="mr-4 h-6 w-6 text-cyan-200"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								aria-hidden="true"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
								/>
							</svg>
							Privacy
						</a>
					</div>
				</div>
			</nav>
		</div>
	</div>

	<div class="lg:pl-64 flex flex-col flex-1">
		<div
			class="relative z-10 flex-shrink-0 flex h-16 bg-white border-b border-gray-200 lg:border-none"
		>
			<button
				type="button"
				class="px-4 border-r border-gray-200 text-gray-400 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-cyan-500 lg:hidden"
			>
				<span class="sr-only">Open sidebar</span>
				<!-- Heroicon name: outline/menu-alt-1 -->
				<svg
					class="h-6 w-6"
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					aria-hidden="true"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M4 6h16M4 12h8m-8 6h16"
					/>
				</svg>
			</button>
			<!-- Search bar -->
			<div class="flex-1 px-4 flex justify-between sm:px-6 lg:max-w-6xl lg:mx-auto lg:px-8">
				<div class="flex-1 flex">
					<form class="w-full flex md:ml-0" action="#" method="GET">
						<label for="search-field" class="sr-only">Search</label>
						<div class="relative w-full text-gray-400 focus-within:text-gray-600">
							<div
								class="absolute inset-y-0 left-0 flex items-center pointer-events-none"
								aria-hidden="true"
							>
								<!-- Heroicon name: solid/search -->
								<svg
									class="h-5 w-5"
									xmlns="http://www.w3.org/2000/svg"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										fill-rule="evenodd"
										d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
										clip-rule="evenodd"
									/>
								</svg>
							</div>
							<input
								id="search-field"
								name="search-field"
								class="block w-full h-full pl-8 pr-3 py-2 border-transparent text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-0 focus:border-transparent sm:text-sm"
								placeholder="Search transactions"
								type="search"
							/>
						</div>
					</form>
				</div>
				<div class="ml-4 flex items-center md:ml-6">
					<button
						type="button"
						class="bg-white p-1 rounded-full text-gray-400 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-cyan-500"
					>
						<span class="sr-only">View notifications</span>
						<!-- Heroicon name: outline/bell -->
						<svg
							class="h-6 w-6"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
							/>
						</svg>
					</button>

					<!-- Profile dropdown -->
					<div class="ml-3 relative">
						<div>
							<button
								type="button"
								class="max-w-xs bg-white rounded-full flex items-center text-sm focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-cyan-500 lg:p-2 lg:rounded-md lg:hover:bg-gray-50"
								id="user-menu-button"
								aria-expanded="false"
								aria-haspopup="true"
								on:click={toggleDropdown}
							>
								<img class="h-8 w-8 rounded-full" src={admin} alt="" />
								<span class="hidden ml-3 text-gray-700 text-sm font-medium lg:block"
									><span class="sr-only">Open user menu for </span>Admin</span
								>
								<!-- Heroicon name: solid/chevron-down -->
								<svg
									class="hidden flex-shrink-0 ml-1 h-5 w-5 text-gray-400 lg:block"
									xmlns="http://www.w3.org/2000/svg"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
										clip-rule="evenodd"
									/>
								</svg>
							</button>
						</div>

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
							class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg py-1 bg-white
                             ring-1 ring-black ring-opacity-5 focus:outline-none"
							style:visibility={isClicked ? 'visible' : 'hidden'}
							role="menu"
							aria-orientation="vertical"
							aria-labelledby="user-menu-button"
							tabindex="-1"
						>
							<!-- Active: "bg-gray-100", Not Active: "" -->
							<a
								href="#"
								class="block px-4 py-2 text-sm text-gray-700"
								role="menuitem"
								tabindex="-1"
								id="user-menu-item-0">Your Profile</a
							>
							<a
								href="#"
								class="block px-4 py-2 text-sm text-gray-700"
								role="menuitem"
								tabindex="-1"
								id="user-menu-item-1">Settings</a
							>
							<a
								href="/"
								class="block px-4 py-2 text-sm text-gray-700"
								role="menuitem"
								tabindex="-1"
								id="user-menu-item-2">Logout</a
							>
						</div>
					</div>
				</div>
			</div>
		</div>
		<main class="flex-1 pb-8">
			<!-- Page header -->
			<div class="bg-white shadow">
				<div class="px-4 sm:px-6 lg:max-w-6xl lg:mx-auto lg:px-8">
					<div
						class="py-6 md:flex md:items-center md:justify-between lg:border-t lg:border-gray-200"
					>
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
				<div class="md:grid md:grid-cols-2 md:divide-x md:divide-gray-200">
					<div class="md:pr-14">
						<div class="flex items-center">
							<h2 class="flex-auto font-semibold text-gray-900 ml-10">January 2022</h2>
							<button
								type="button"
								class="-my-1.5 flex flex-none items-center justify-center p-1.5 text-gray-400 hover:text-gray-500"
							>
								<span class="sr-only">Previous month</span>
								<!-- Heroicon name: solid/chevron-left -->
								<svg
									class="h-5 w-5"
									xmlns="http://www.w3.org/2000/svg"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										fill-rule="evenodd"
										d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
										clip-rule="evenodd"
									/>
								</svg>
							</button>
							<button
								type="button"
								class="-my-1.5 -mr-1.5 ml-2 flex flex-none items-center justify-center p-1.5 text-gray-400 hover:text-gray-500"
							>
								<span class="sr-only">Next month</span>
								<!-- Heroicon name: solid/chevron-right -->
								<svg
									class="h-5 w-5"
									xmlns="http://www.w3.org/2000/svg"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										fill-rule="evenodd"
										d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
										clip-rule="evenodd"
									/>
								</svg>
							</button>
						</div>
						<div class="mt-10 grid grid-cols-7 text-center text-xs leading-6 text-gray-500">
							<div>M</div>
							<div>T</div>
							<div>W</div>
							<div>T</div>
							<div>F</div>
							<div>S</div>
							<div>S</div>
						</div>
						<div class="mt-2 grid grid-cols-7 text-sm">
							<div class="py-2">
								<!--
                            Always include: "mx-auto flex h-8 w-8 items-center justify-center rounded-full"
                            Is selected, include: "text-white"
                            Is not selected and is today, include: "text-indigo-600"
                            Is not selected and is not today and is current month, include: "text-gray-900"
                            Is not selected and is not today and is not current month, include: "text-gray-400"
                            Is selected and is today, include: "bg-indigo-600"
                            Is selected and is not today, include: "bg-gray-900"
                            Is not selected, include: "hover:bg-gray-200"
                            Is selected or is today, include: "font-semibold"
                          -->
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2021-12-27">27</time>
								</button>
							</div>
							<div class="py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2021-12-28">28</time>
								</button>
							</div>
							<div class="py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2021-12-29">29</time>
								</button>
							</div>
							<div class="py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2021-12-30">30</time>
								</button>
							</div>
							<div class="py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2021-12-31">31</time>
								</button>
							</div>
							<div class="py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-01">1</time>
								</button>
							</div>
							<div class="py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-02">2</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-03">3</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-04">4</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-05">5</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-06">6</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-07">7</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-08">8</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-09">9</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-10">10</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-11">11</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full font-semibold text-indigo-600 hover:bg-gray-200"
								>
									<time datetime="2022-01-12">12</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-13">13</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-14">14</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-15">15</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-16">16</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-17">17</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-18">18</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-19">19</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-20">20</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full bg-gray-900 font-semibold text-white"
								>
									<time datetime="2022-01-21">21</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-22">22</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-23">23</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-24">24</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-25">25</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-26">26</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-27">27</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-28">28</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-29">29</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-30">30</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-900 hover:bg-gray-200"
								>
									<time datetime="2022-01-31">31</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2022-02-01">1</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2022-02-02">2</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2022-02-03">3</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2022-02-04">4</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2022-02-05">5</time>
								</button>
							</div>
							<div class="border-t border-gray-200 py-2">
								<button
									type="button"
									class="mx-auto flex h-8 w-8 items-center justify-center rounded-full text-gray-400 hover:bg-gray-200"
								>
									<time datetime="2022-02-06">6</time>
								</button>
							</div>
						</div>
					</div>
					<section class="mt-12 md:mt-0 md:pl-14">
						<h2 class="font-semibold text-gray-900">
							Schedule for <time datetime="2022-01-21">January 21, 2022</time>
						</h2>
						<ol class="mt-4 space-y-1 text-sm leading-6 text-gray-500">
							<li
								class="group flex items-center space-x-4 rounded-xl py-2 px-4 focus-within:bg-gray-100 hover:bg-gray-100"
							>
								<img
									src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
									alt=""
									class="h-10 w-10 flex-none rounded-full"
								/>
								<div class="flex-auto">
									<p class="text-gray-900">Leslie Alexa</p>
									<p class="mt-0.5">
										<time datetime="2022-01-21T13:00">1:00 PM</time> -
										<time datetime="2022-01-21T14:30">2:30 PM</time>
									</p>
								</div>
								<div class="relative opacity-0 focus-within:opacity-100 group-hover:opacity-100">
									<div>
										<button
											type="button"
											class="-m-2 flex items-center rounded-full p-1.5 text-gray-500 hover:text-gray-600"
											id="menu-0-button"
											aria-expanded="false"
											aria-haspopup="true"
										>
											<span class="sr-only">Open options</span>
											<!-- Heroicon name: outline/dots-vertical -->
											<svg
												class="h-6 w-6"
												xmlns="http://www.w3.org/2000/svg"
												fill="none"
												viewBox="0 0 24 24"
												stroke="currentColor"
												aria-hidden="true"
											>
												<path
													stroke-linecap="round"
													stroke-linejoin="round"
													stroke-width="2"
													d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z"
												/>
											</svg>
										</button>
									</div>

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
										class="focus:outline-none absolute right-0 z-10 mt-2 w-36 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5"
										role="menu"
										aria-orientation="vertical"
										aria-labelledby="menu-0-button"
										tabindex="-1"
									>
										<div class="py-1" role="none">
											<!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
											<a
												href="#"
												class="text-gray-700 block px-4 py-2 text-sm"
												role="menuitem"
												tabindex="-1"
												id="menu-0-item-0">Edit</a
											>
											<a
												href="#"
												class="text-gray-700 block px-4 py-2 text-sm"
												role="menuitem"
												tabindex="-1"
												id="menu-0-item-1">Cancel</a
											>
										</div>
									</div>
								</div>
							</li>

							<!-- More meetings... -->
						</ol>
					</section>
				</div>
			</div>
		</main>
	</div>
</div>
