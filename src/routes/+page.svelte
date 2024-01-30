<script>
    import { onMount } from 'svelte';
  import { goto } from '$app/navigation';
 

</script>

<div class="flex flex-row h-dvh">
  <div class="basis-2/5 bg-blue-500 flex flex-col relative">
    <div class="absolute top-80 left-1/4 font-sans text-4xl text-white">
      welcome to page
    </div>
    <div class="absolute top-1/2 left-1/3"><p class="px-8 mt-6 ">sign in to continue access</p></div>
  </div>
  <div class="  basis-3/5 relative bg-white">
    <div
      class="flex flex-col justify-center h-auto w-1/3 top-1/3 left-1/3 absolute"
    >
      <h2 class="text-2xl font-bold mb-6 text-center">Sign In</h2>
      <div class="mb-1">
        <label for="username" class="block text-sm font-medium text-gray-600"
          >User Name</label
        >
        <input
          type="text"
          id="username"
          name="username"
          class="mt-1 w-full border border-black text-xs p-1 text-center"
          placeholder="Enter your username"
        />
      </div>
      <div class="mb-1">
        <label for="username" class="block text-sm font-medium text-gray-600"
          >User Id</label
        >
        <input
          type="text"
          id="username"
          name="username"
          class="mt-1 w-full border border-black text-xs p-1 text-center"
          placeholder="Enter your user Id"
        />
      </div>
      <button class="bg-blue-500 text-white p-1 w-full mt-4" on:click={() => goto('/record-view-page')}>Login</button>

      <div class="flex items-center mt-4">
        <hr class="flex-grow border-t border-gray-300" />
        <span class="mx-4 text-gray-500">or</span>
        <hr class="flex-grow border-t border-gray-300" />
      </div>

      <button
        class="bg-blue-500 text-white p-1 flex justify-center items-center space-x-2 mt-4"
      >
        <i class="fa-brands fa-google"></i>
        <!-- Google Icon from FontAwesome -->
        <span>Sign in with Google</span>
      </button>
      <div class="flex items-center justify-center">
        <span class="mr-2">Not a member?</span>
        <button class="text-blue-500 hover:underline focus:outline-none " on:click={() => goto('/register-page')}>
          Create Account
        </button>
      </div>
    </div>
  </div>
</div>
