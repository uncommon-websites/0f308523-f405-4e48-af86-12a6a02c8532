<script>
  // No script needed
</script>

<div class="space-y-32 pb-32">
  <!-- Early-Stage Capital Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Early-Stage Capital</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Patient funding for hardware timelines.</strong> We provide multi-stage capital commitments that understand the realities of building physical infrastructure—from prototype to production scale.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Investment Approach 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View portfolio</a>
      </div>
    </div>
    <div class="bg-gray-50 rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Investment Stage Visualization -->
      <div class="relative w-full max-w-md">
        <div class="space-y-6">
          {#each [
            { stage: 'Seed', amount: '$500K - $2M', focus: 'Prototype & validation' },
            { stage: 'Series A', amount: '$5M - $15M', focus: 'Production scaling' },
            { stage: 'Series B', amount: '$20M - $50M', focus: 'Market expansion' }
          ] as round, i}
            <div class="flex items-center gap-4">
              <div class="w-12 h-12 bg-black rounded-lg flex items-center justify-center text-white font-bold text-sm shrink-0">
                {i + 1}
              </div>
              <div class="flex-1">
                <div class="font-medium text-lg mb-1">{round.stage}</div>
                <div class="text-sm text-gray-600">{round.amount}</div>
                <div class="text-xs text-gray-500 mt-1">{round.focus}</div>
              </div>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </section>

  <!-- Operational Support Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Operational Expertise</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Beyond capital.</strong> Our team brings decades of experience scaling hardware companies, navigating government contracts, and building supply chains—so you can focus on your product and mission.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Meet the team 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">Resources</a>
      </div>
    </div>
    <div class="bg-gray-50 rounded-3xl overflow-hidden min-h-[400px] relative p-12">
      <div class="space-y-4">
        {#each [
          'Supply chain optimization',
          'Government contracting',
          'Manufacturing partnerships',
          'Regulatory navigation',
          'Talent acquisition',
          'Strategic introductions'
        ] as capability}
          <div class="flex items-center gap-3 p-3 bg-white rounded-lg border border-gray-200">
            <div class="w-2 h-2 bg-black rounded-full"></div>
            <span class="text-sm font-medium">{capability}</span>
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- Network Access Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Strategic Network</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Connections that matter.</strong> Access to defense primes, government decision-makers, and fellow founders building the future of American infrastructure and national security.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Join our community 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">Events</a>
      </div>
    </div>
    <div class="bg-black rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Network Visualization -->
      <div class="relative w-full h-full flex items-center justify-center">
        <!-- Central node -->
        <div class="absolute w-20 h-20 bg-white rounded-full flex items-center justify-center z-10">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="black"><path d="M3 3h7v7H3V3zm11 0h7v7h-7V3zm0 11h7v7h-7v-7zM3 14h7v7H3v-7z"/></svg>
        </div>
        
        <!-- Orbiting nodes -->
        {#each Array(8) as _, i}
          <div 
            class="absolute w-12 h-12 bg-gray-800 rounded-full border-2 border-gray-700"
            style="
              transform: rotate({i * 45}deg) translateX(120px) rotate(-{i * 45}deg);
            "
          ></div>
        {/each}
      </div>
    </div>
  </section>
</div>
