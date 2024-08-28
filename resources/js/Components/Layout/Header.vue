<script setup>
import { Link } from "@inertiajs/vue3";
import { CircleUser, Menu, Package2, Search } from "lucide-vue-next";
import { Button } from "@/Components/ui/button";
import { Input } from "@/Components/ui/input";
import { Sheet, SheetContent, SheetTrigger } from "@/Components/ui/sheet";
import {
    DropdownMenu,
    DropdownMenuContent,
    DropdownMenuItem,
    DropdownMenuLabel,
    DropdownMenuSeparator,
    DropdownMenuTrigger,
} from "@/Components/ui/dropdown-menu";
</script>

<template>
    <header
        class="flex h-14 items-center gap-4 border-b bg-muted/40 px-4 lg:h-[60px] lg:px-6"
    >
        <Sheet>
            <SheetTrigger as-child>
                <Button
                    variant="outline"
                    size="icon"
                    class="shrink-0 md:hidden"
                >
                    <Menu class="h-5 w-5" />
                    <span class="sr-only">Toggle navigation menu</span>
                </Button>
            </SheetTrigger>
            <SheetContent side="left" class="flex flex-col">
                <nav class="grid gap-2 text-lg font-medium">
                    <a
                        href="#"
                        class="flex items-center gap-2 text-lg font-semibold"
                    >
                        <Package2 class="h-6 w-6" />
                        <span class="sr-only">Acme Inc</span>
                    </a>
                    <!-- Add other nav links here -->
                </nav>
            </SheetContent>
        </Sheet>
        <div class="w-full flex-1">
            <form>
                <div class="relative">
                    <Search
                        class="absolute left-2.5 top-2.5 h-4 w-4 text-muted-foreground"
                    />
                    <Input
                        type="search"
                        placeholder="Search products..."
                        class="w-full appearance-none bg-background pl-8 shadow-none md:w-2/3 lg:w-1/3"
                    />
                </div>
            </form>
        </div>
        <DropdownMenu>
            <DropdownMenuTrigger as-child>
                <Button variant="secondary" size="icon" class="rounded-full">
                    <CircleUser class="h-5 w-5" />
                    <span class="sr-only">Toggle user menu</span>
                </Button>
            </DropdownMenuTrigger>
            <DropdownMenuContent align="end">
                <DropdownMenuLabel>My Account</DropdownMenuLabel>
                <DropdownMenuSeparator />
                <DropdownMenuItem>Settings</DropdownMenuItem>
                <Link :href="route('profile.edit')"
                    ><DropdownMenuItem>Profile</DropdownMenuItem></Link
                >
                <DropdownMenuSeparator />
                <Link :href="route('logout')" method="post" as="button"
                    ><DropdownMenuItem>Logout</DropdownMenuItem></Link
                >
            </DropdownMenuContent>
        </DropdownMenu>
    </header>
</template>
