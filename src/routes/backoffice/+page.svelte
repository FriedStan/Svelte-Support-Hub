<script>
    import LdapButton from "$lib/feature-button/LdapButton.svelte";
    import RequestButton from "$lib/feature-button/RequestButton.svelte";
    import VMButton from "$lib/feature-button/VMButton.svelte";
    import NetBlockerButton from "$lib/feature-button/NetBlockerButton.svelte";
</script>

<div class="min-h-screen pt-5">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8 sm:py-12">
        <!-- Enhanced header with statistics -->
        <div class="text-center mb-12 relative overflow-hidden">
            <!-- Main header content -->
            <div class="relative z-10">
                <h1 class="text-3xl sm:text-4xl lg:text-5xl font-bold bg-gradient-to-r from-gray-800 to-gray-600 bg-clip-text text-transparent mb-4">
                    ระบบจัดการกลาง
                </h1>
                <p class="text-lg sm:text-xl text-gray-600 max-w-2xl mx-auto leading-relaxed">
                    จัดการระบบ IT Support Hub อย่างมีประสิทธิภาพด้วยเครื่องมือที่ครบครัน
                </p>
            </div>
        </div>
        <div class="bg-white rounded-3xl shadow-xl border border-gray-100 overflow-hidden">
            <div class="p-8 sm:p-10">
                <h2 class="text-2xl font-bold text-gray-800 mb-8 text-center">เครื่องมือจัดการ</h2>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                    <LdapButton />
                    <RequestButton />
                    <VMButton />
                    <NetBlockerButton />
                </div>
            </div>
        </div>
    </div>
</div>