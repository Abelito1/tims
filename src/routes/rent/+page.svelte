<script>
	import admin from '$lib/images/Admin-Profile.png';
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
										APPLICATION REQUEST
									</h1>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</main>
	<div class="flex flex-col">
		<div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
			<div class="py-2 align-middle inline-block min-w-full sm:px-6 lg:px-8">
				<div class="shadow overflow-hidden border-b border-gray-200 sm:rounded-lg">
					<table class="min-w-full divide-y divide-gray-200">
						<thead class="bg-gray-50">
							<tr>
								<th
									scope="col"
									class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
									>Name</th
								>
								<th
									scope="col"
									class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
									>Title</th
								>
								<th
									scope="col"
									class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
									>Email</th
								>
								<th
									scope="col"
									class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
									>Role</th
								>
								<th scope="col" class="relative px-6 py-3">
									<span class="sr-only">Edit</span>
								</th>
							</tr>
						</thead>
						<tbody class="bg-white divide-y divide-gray-200">
							<tr>
								<td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900"
									>Jane Cooper</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500"
									>Regional Paradigm Technician</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500"
									>jane.cooper@example.com</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Admin</td>
								<td class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium">
									<a href="#" class="text-indigo-600 hover:text-indigo-900">Edit</a>
								</td>
							</tr>

							<tr>
								<td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900"
									>Gerecha Bermiso</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500"
									>Regional Paradigm Technician</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500"
									>gerecha.bermiso@example.com</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Admin</td>
								<td class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium">
									<a href="#" class="text-indigo-600 hover:text-indigo-900">Edit</a>
								</td>
							</tr>

							<tr>
								<td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900"
									>Dexter Casinillo</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500"
									>Regional Paradigm Technician</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500"
									>Dexter.casinillo@example.com</td
								>
								<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">Admin</td>
								<td class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium">
									<a href="#" class="text-indigo-600 hover:text-indigo-900">Edit</a>
								</td>
							</tr>

							<!-- More people... -->
						</tbody>
					</table>
				</div>
			</div>
		</div>
	</div>
</div>
