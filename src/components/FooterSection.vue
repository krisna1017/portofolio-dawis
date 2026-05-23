<template>
  <section id="contact" class="relative h-full px-12 py-12 rounded-t-4xl bg-black inset-shadow-sm inset-shadow-neutral-500 text-white font-poppins backdrop-blur-3xl">
    <!-- <div class="absolute inset-x-0 top-0 h-40 bg-[radial-gradient(circle_at_top_left,rgba(16,185,129,0.16),transparent_35%),radial-gradient(circle_at_top_right,rgba(56,189,248,0.12),transparent_30%)] pointer-events-none"></div> -->
    <div class="container mx-auto relative z-10 px-4 md:px-14">
      <div class="flex flex-col gap-12 justify-center md:flex-row md:items-center md:justify-between">
        <div class="max-w-xl space-y-8">
          <div>
            <h2 class="mt-4 text-2xl font-regular tracking-wider text-green-400 md:text-4xl uppercase font-anton">Portofolio Dawista</h2>
          </div>

          <div class="grid sm:grid-cols-1">
            <a href="mailto:ikadekdawista@gmail.com" class="group flex items-center gap-2">
              <span class="inline-flex h-11 w-11 items-center justify-center rounded-full bg-gray-300 text-green-600 transition group-hover:bg-emerald-500/25">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="h-5 w-5 fill-current"><path d="M2.25 6.75A2.25 2.25 0 014.5 4.5h15a2.25 2.25 0 012.25 2.25v10.5A2.25 2.25 0 0119.5 19.5h-15A2.25 2.25 0 012.25 16.5V6.75zm2.25-.75L12 11.25 19.5 6h-15zM4.5 7.678v8.822l6.992-5.028L4.5 7.678zm7.478 4.497L19.5 16.5V7.678l-7.522 4.497z"/></svg>
              </span>
              <div>
                <p class="text-sm md:text-base font-bold text-gray-200 tracking-wider">ikadekdawista@gmail.com</p>
              </div>
            </a>

            <a href="https://instagram.com/kdkws_" target="_blank" rel="noreferrer" class="group flex items-center gap-2 py-4">
              <span class="inline-flex h-11 w-11 items-center justify-center rounded-full bg-gray-300 text-green-600 transition group-hover:bg-cyan-500/25">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="h-6 w-6 fill-current"><path d="M7.5 2.25h9A5.25 5.25 0 0121.75 7.5v9a5.25 5.25 0 01-5.25 5.25h-9A5.25 5.25 0 012.25 16.5v-9A5.25 5.25 0 017.5 2.25zm0 1.5A3.75 3.75 0 003.75 7.5v9A3.75 3.75 0 007.5 20.25h9a3.75 3.75 0 003.75-3.75v-9A3.75 3.75 0 0016.5 3.75h-9zm4.5 2.25a5.25 5.25 0 110 10.5 5.25 5.25 0 010-10.5zm0 1.5a3.75 3.75 0 100 7.5 3.75 3.75 0 000-7.5zm4.875-.75a1.125 1.125 0 110 2.25 1.125 1.125 0 010-2.25z"/></svg>
              </span>
              <div>
                <p class="text-sm md:text-base font-bold text-gray-200 tracking-wider">kdkws_</p>
              </div>
            </a>

            <a href="https://wa.me/62895354768641" target="_blank" rel="noreferrer" class="group flex items-center gap-2 transition">
              <span class="inline-flex h-11 w-11 items-center justify-center rounded-full bg-gray-300 text-green-600 transition group-hover:bg-emerald-400/25">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="h-6 w-6 fill-current"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.472-.148-.672.15-.198.297-.768.967-.94 1.166-.173.198-.347.223-.644.075-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.447-.52.149-.173.198-.297.298-.495.099-.198.05-.372-.025-.52-.075-.149-.672-1.615-.92-2.213-.242-.582-.487-.502-.672-.512l-.573-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.485.709.306 1.262.489 1.693.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414-.075-.124-.273-.198-.57-.347z"/></svg>
              </span>
              <div>
                <p class="text-sm md:text-base font-bold text-gray-200 tracking-wider">0895354768641</p>
              </div>
            </a>
          </div>
        </div>

        <div class="hidden md:flex items-center justify-center">
          <div class="relative h-72 w-72 overflow-hidden rounded-full border-14 border-black bg-white/5 shadow-[0_40px_120px_rgba(0,0,0,0.4)]">
            <img src="/image/profile.jpeg" alt="Profile" class="h-full w-full object-cover" />
            <div class="absolute inset-x-0 bottom-0 h-24 bg-linear-to-t from-slate-950/95 via-transparent to-transparent"></div>
          </div>
        </div>
      </div>

      <div class="mt-10 border-t border-white pt-6 text-center text-sm text-slate-400">
        © 2025 Graphy. All rights reserved.
      </div>
    </div>
  </section>
</template>

