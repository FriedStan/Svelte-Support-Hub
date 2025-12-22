<script lang="ts">
    import ITLogo from "$lib/assets/img/it-logo.png";
    import XIcon from "@lucide/svelte/icons/x";
    import { Button } from "$lib/components/ui/button/index.js";
    import { Input } from "$lib/components/ui/input/index.js";
    import * as Card from "$lib/components/ui/card/index.js";
    import { Eye, EyeOff } from "@lucide/svelte/icons";

    let showPassword = false;
</script>
 
<Card.Root class="-my-4 w-full max-w-sm">
 <Card.Header>
    <div class="flex items-center justify-center">
        <img class="w-20 ml-15" src="{ ITLogo }" alt="">
    </div>
  <Card.Action>
   <Button variant="link" class="cursor-pointer"><XIcon /></Button>
  </Card.Action>
  <Card.Title class="text-2xl font-semibold ml-20">Account Log In</Card.Title>
 </Card.Header>
 <Card.Content class="pb-4">
  <form>
   <div class="flex flex-col gap-6">
    <div class="grid gap-2">
     <Input class="h-12" id="email" type="email" placeholder="Username" required />
    </div>
    <div class="grid gap-2">
     <Input class="h-12" id="password" type="password" placeholder="Password" required />
     <Button><Eye/></Button>
    </div>
   </div>
  </form>
 </Card.Content>
 <Card.Footer class="flex-col gap-2">
  <Button type="submit" class="w-full">Login</Button>
  <Button variant="outline" class="w-full">Login with Google</Button>
 </Card.Footer>
</Card.Root>