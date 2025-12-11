<script lang="ts">
    import { Label, Select } from "flowbite-svelte";
    import interfacesData from "$lib/interfaces_ex.json";
    let srcIntf: string = "";

    let interfaces = interfacesData.results;
</script>

<header
    class="bg-gradient-to-r from-blue-500 to-indigo-600 py-20 md:py-28 text-white relative overflow-hidden"
>
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden opacity-10">
        <i
            class="fas fa-laptop text-white absolute top-10 left-10 text-6xl transform -rotate-12 bg-icon"
        ></i>
        <i
            class="fas fa-server text-white absolute top-40 right-20 text-5xl bg-icon"
        ></i>
        <i
            class="fas fa-network-wired text-white absolute bottom-20 left-1/4 text-4xl transform rotate-12 bg-icon"
        ></i>
        <i
            class="fas fa-globe text-white absolute bottom-40 right-1/3 text-5xl bg-icon"
        ></i>
    </div>

    <div class="container mx-auto px-6 text-center relative z-10">
        <div
            class="inline-block mb-6 bg-white/20 backdrop-blur-sm px-4 py-2 rounded-full"
        >
            <span class="text-white flex items-center justify-center">
                <i class="fas fa-headset mr-2"></i> ระบบคำขอบริการ IT Support ใหม่กว่า
            </span>
        </div>

        <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
            ITSupportHub: <span class="text-blue-200"
                >ศูนย์กลางคำขอบริการ IT</span
            >
        </h1>
        <p
            class="text-lg md:text-xl text-blue-100 mb-10 max-w-3xl mx-auto leading-relaxed"
        >
            ระบบสำหรับยื่นคำร้องขอยืมอุปกรณ์ไอที, ขอใช้งาน Virtual Machine (VM),
            และขอ Subdomain พร้อมติดตามสถานะคำขอของคุณแบบเรียลไทม์
        </p>
    </div>
</header>

<div>
    <Label>
        Select an option
        <Select class="mt-2" items={interfaces.map((inf) => ({
            value: inf.q_origin_key, name: inf.name
        }))} bind:value={srcIntf} />
    </Label>
</div>
