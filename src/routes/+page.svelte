<script>
	import logo from '$lib/images/timslogo.png';
	import bus from '$lib/images/bus.jpg';
</script>

<body>
	<div class="absolute inset-0 -z-10">
		<img class="h-full w-full object-cover" src={bus} alt="People working on laptops" />
		<div class="absolute inset-0 bg-gray-500 mix-blend-multiply" />
	</div>
	<div class="min-h-full flex flex-col justify-center py-12 sm:px-6 lg:px-8">
		<div class="sm:mx-auto sm:w-full sm:max-w-md">
			<img class="mx-auto h-32 w-auto" src={logo} alt="Workflow" />
			<h2 class="mt-6 text-center text-3xl font-semibold text-white">INHITRANSCO Admin</h2>
		</div>

		<div class="mt-8 sm:mx-auto sm:w-full sm:max-w-md">
			<div class="bg-white py-16 px-4 shadow sm:rounded-lg sm:px-10">
				<form class="space-y-6" action="#" method="POST">
					<div>
						<label for="email" class="block text-sm font-medium text-gray-700"> Username </label>
						<div class="mt-1">
							<input
								id="email"
								name="email"
								type="email"
								autocomplete="email"
								required
								placeholder="Enter your username"
								class="appearance-none block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm placeholder-gray-400 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm"
							/>
						</div>
					</div>

					<div>
						<label for="password" class="block text-sm font-medium text-gray-700"> Password </label>
						<div class="mt-1">
							<input
								id="password"
								name="password"
								type="password"
								autocomplete="current-password"
								required
								placeholder="Enter your password"
								class="appearance-none block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm placeholder-gray-400 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm"
							/>
						</div>
					</div>

					<div class="flex items-center justify-between">
						<div class="flex items-center">
							<input
								id="remember-me"
								name="remember-me"
								type="checkbox"
								class="h-4 w-4 text-gray-600 focus:ring-gray-500 border-gray-300 rounded"
							/>
							<label for="remember-me" class="ml-2 block text-sm text-gray-900">
								Remember me
							</label>
						</div>

						<div class="text-sm">
							<a href="#" class="font-medium text-gray-500 hover:text-gray-800">
								Forgot your password?
							</a>
						</div>
					</div>

					<div>
						<!-- <button
						type="submit"
						class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
						>Sign in</button
					> -->
						<a
							href="/dashboard"
							class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-gray-500 hover:bg-gray-600 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
							>Sign in</a
						>
					</div>
				</form>
			</div>
		</div>
	</div>
</body>
