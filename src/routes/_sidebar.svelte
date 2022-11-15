<script>
	import logo from '$lib/images/timslogo.png';
	import { page } from '$app/stores';

	let isClicked = false;

	function toggleDropdown() {
		isClicked = !isClicked;
	}
</script>

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
	<div class="fixed inset-0 bg-opacity-75" aria-hidden="true" />

	<!--
        Off-canvas menu, show/hide based on off-canvas menu state.
  
        Entering: "transition ease-in-out duration-300 transform"
          From: "-translate-x-full"
          To: "translate-x-0"
        Leaving: "transition ease-in-out duration-300 transform"
          From: "translate-x-0"
          To: "-translate-x-full"
      -->
	<div class="flex flex-col flex-grow bg-gray-600 pt-5 pb-4 overflow-y-auto hidden">
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
			<img class="h-24 w-auto mx-auto" src={logo} alt="Easywire logo" />
		</div>
		<nav class="mt-5 flex-shrink-0 h-full divide-y  overflow-y-auto" aria-label="Sidebar">
			<div class="px-2 space-y-1">
				<!-- Current: "bg-cyan-800 text-white", Default: "text-cyan-100 hover:text-white hover:bg-cyan-600" -->
				<a
					href="/dashboard"
					class="bg-cyan-500 text-white group flex items-center px-2 py-2 text-base font-medium rounded-md"
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
					href="/applicant"
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
					applicant
				</a>

				<a
					href="/records"
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
					Records
				</a>

				<a
					href="/inhitransco"
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
					INHITRANSCO
				</a>

				<a
					href="/file"
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
					File Manager
				</a>

				<a
					href="executive"
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
					Executive
				</a>
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
					class=" text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md
                    {$page.url.pathname == '/dashboard' ? 'bg-cyan-600 text-white' : ''}"
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
					href="/applicant"
					class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md
                    {$page.url.pathname == '/applicant' ? 'bg-cyan-600 text-white' : ''}"
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
							fill="currentColor"
							d="M7 2a2 2 0 0 0-2 2H4a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h1a2 2 0 0 0 2 2h6a2 2 0 0 0 2-2h1a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2h-1a2 2 0 0 0-2-2H7Zm8 3h1a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-1V5ZM5 15H4a1 1 0 0 1-1-1V6a1 1 0 0 1 1-1h1v10ZM6 4a1 1 0 0 1 1-1h6a1 1 0 0 1 1 1v12a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V4Z"
						/>
					</svg>
					Applicant
				</a>

				<a
					href="/records"
					class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md
                    {$page.url.pathname == '/records' ? 'bg-cyan-600 text-white' : ''}"
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
					href="/inhitransco"
					class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md
                    {$page.url.pathname == '/inhitransco' ? 'bg-cyan-600 text-white' : ''}"
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
					INHITRANSCO
				</a>

				<a
					href="/file"
					class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md
                    {$page.url.pathname == '/file' ? 'bg-cyan-600 text-white' : ''}"
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
							fill="currentColor"
							d="M2.165 19.551c.186.28.499.449.835.449h15c.4 0 .762-.238.919-.606l3-7A.998.998 0 0 0 21 11h-1V8c0-1.103-.897-2-2-2h-6.655L8.789 4H4c-1.103 0-2 .897-2 2v13h.007a1 1 0 0 0 .158.551zM18 8v3H6c-.4 0-.762.238-.919.606L4 14.129V8h14z"
						/>
					</svg>
					File manager
				</a>

				<a
					href="/executive"
					class="text-cyan-100 hover:text-white hover:bg-cyan-600 group flex items-center px-2 py-2 text-sm leading-6 font-medium rounded-md
                    {$page.url.pathname == '/executive' ? 'bg-cyan-600 text-white' : ''}"
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
							d="M9 11a4 4 0 1 0-4-4a4 4 0 0 0 4 4Zm8 2a3 3 0 1 0-3-3a3 3 0 0 0 3 3Zm4 7a1 1 0 0 0 1-1a5 5 0 0 0-8.06-3.95A7 7 0 0 0 2 20a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1"
						/>
					</svg>
					Executives
				</a>
			</div>
		</nav>
	</div>
</div>
