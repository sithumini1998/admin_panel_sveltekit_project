<script>
  import { onMount } from "svelte";
  import { goto } from "$app/navigation";
  import iconOne from "$lib/assets/219_visa.jpg";
  import iconTwo from "$lib/assets/ca0c7039ddcf224cb6b075cb59e4677e.jpg";
</script>

<div class="flex flex-row h-dvh">
  <div class="basis-1/2 relative">
    <div
      class="absolute flex flex-col top-1/3 left-1/3 w-1/2 h-auto "
    >
      <div class="mb-4">
        <label for="username" class="block text-sm font-medium text-gray-600"
          >User Id</label
        >
        <input
          type="text"
          id="username"
          name="username"
          class="mt-1 w-full border border-black text-xs p-1 text-center"
          placeholder="Leave to Empty Autogenerate"
        />
      </div>
      <div class="mb-5">
        <label for="userRole" class="block text-sm font-medium text-gray-600"
          >Currency Type</label
        >
        <select
          id="userRole"
          name="userRole"
          class="mt-1 w-full border border-black text-xs p-1"
        >
          <option value="admin">LKR</option>
          <option value="user">USD</option>
        </select>
      </div>
      <div class="mb-5">
        <label for="username" class="block text-sm font-medium text-gray-600"
          >Price</label
        >
        <input
          type="text"
          id="username"
          name="username"
          class="mt-1 w-full border border-black text-xs p-1 text-center"
          placeholder="Enter Price"
        />
      </div>

      <!-- Dropdown menu example -->
      
    </div>
    <button
      class="bg-red-500 text-white px-6 py-2 rounded-md hover:bg-green-600 focus:outline-none absolute top-2/3 left-1/2"
      >Cancel</button
    >
  </div>
  <div class="basis-1/2 relative">
    <div
      class="absolute flex flex-col top-1/3 right-1/3 w-1/2 h-auto bg-purple-200 p-5 rounded-md"
    >
      <div class="flex flex-row justify-between">
        <p class="w-auto h-auto">payment methode</p>
        <div class="w-20 h-auto border border-black">
          <img src={iconOne} alt="Icon" class="w-full h-8 mr-2" />
        </div>
        <div class="w-20 h-auto border border-black">
          <img src={iconTwo} alt="Icon" class="w-full h-8 mr-2" />
        </div>
      </div>
      <div class="mt-2">
        <input
          type="text"
          id="name"
          name="name"
          class="mt-4 w-full border border-black text-xs p-1 text-center placeholder-gray-400"
          placeholder="card number"
        />
      </div>
      <div class="flex flex-row justify-between mt-10">
        <div class="w-20 h-auto border border-black flex items-center justify-center">Expriry</div>
        <div class="flex items-center justify-center">
            <div class="w-20 h-auto border border-black flex items-center justify-center">CVC</div>
        <p class="w-auto h-auto text-xs leading-tight ml-2 ">
          3 digit code on<br />the back of your card
        </p>
        </div>
        
      </div>
      
      <div class="mt-2 flex items-center">
        <input type="checkbox" id="terms" name="terms" class="mr-2" />
        <label for="terms" class="text-sm font-medium text-gray-600">
          Save my card details for faster checkout
        </label>
      </div>

      <!-- Save button -->
    </div>
    <button
      class="bg-green-500 text-white px-6 py-2 rounded-md hover:bg-green-600 focus:outline-none absolute top-2/3 right-1/2"
      on:click={() => goto("/point-view-page")}>Next</button
    >
  </div>
</div>
