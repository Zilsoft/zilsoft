<script>
  import Step from "./Step.svelte";
  let steps = [
    {
      name: "Диагностика ПТСР",
      icon: "fa-solid fa-brain",
      href: "https://mental.crimea-rehab.ru/home/ptsd",
    },
    {
      name: "Технологии питания",
      icon: "fa-solid fa-utensils",
      href: "http://147.45.150.124:8080/config",
    },
    {
      name: "Медицинская реабилитация",
      icon: "fa-solid fa-hand-holding-medical",
      href: "https://crimea-rehab.ru/",
    },
  ];
  let benefits = [
    {
      name: "разработчик-самоучка",
      description:
        "я выбрал путь самостоятельного обучения в сфере программирования и разработки. Это не просто профессия, а результат целеустремленности, любознательности и стремления к самосовершенствованию. Не имея классического образование в сфере-IT, я компенсировал его постоянной практикой, экспериментами и изучением новых технологий. Мои знания часто приобретены через книги, онлайн-курсы, документацию, форумы и собственные проекты, что делает мой опыт уникальным и многогранным.",
    },
    {
      name: "включен от идеи до реализации",
      description:
        "это значит быть полностью погруженным в процесс, понимать все его аспекты и уметь адаптироваться к изменениям на каждом этапе. Это подразумевает не только способность придумать что-то новое, но и готовность взять на себя технические, организационные или даже административные задачи для достижения конечной цели. Такой уровень вовлеченности часто требует сочетания разных качеств: креативности для создания идей, аналитического мышления для их проработки, а также терпения и внимания к деталям для успешного завершения проекта. Это делает человека универсальным звеном в команде или самостоятельным исполнителем, который может довести дело до логического завершения, сохраняя верность изначальной задумке.",
    },
    {
      name: 'работа в команде - "не моё"',
      description:
        "для меня работа в команде — это не то, что действительно зажигает мой интерес или помогает раскрыть весь мой потенциал. Я чувствую себя гораздо более комфортно и продуктивно, когда могу сосредоточиться на задачах самостоятельно, без необходимости постоянно координироваться с другими людьми. Это не значит, что я против сотрудничества как такового, просто мне ближе автономный подход, где я могу принимать решения сам, двигаться своим темпом и не зависеть от чужих мнений или графиков. Для меня важно иметь возможность полностью погрузиться в процесс, не отвлекаясь на обсуждения или компромиссы, которые неизбежны в коллективной работе.",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gam-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Привет! Меня зовут <span class="lato text-violet-400">Дмитрий</span>
        Павлюков<br />Разработчик
        <span class="lato text-violet-400">полного стека</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        Мой <span class="text-violet-400">сновной стек</span> включает
        <br />Frontend: JavaScript, SvelteKit, TailwindCSS<br />Backend:
        PostgreSQL, FastAPI
      </p>
      <a
        href="#link"
        aria-label="Связаться"
        class="blueShadow mx-auto lg:ml-0 text-base sm:text-lg md:text-xl lato relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
        ></div>
        <h4 class="relative z-9">Связяться &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img
        src="/images/profile.png"
        alt="Фото профиля"
        class="object-cover z-2"
      />
    </div>
  </section>
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        Несколько моих творческих начинаний.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Хотите <splan class="lato text-violet-400">посмотреть</splan> на мою работу?
      </h3>
    </div>
    <a
      href="#work"
      aria-label="Мои работы"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-regular fa-circle-play"></i>
      <p>Смотреть работы</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          Проект разрабатывается сотрудниками и учащимися
          <strong class="text-violet-400"
            >Крымского федерального университета им. В.И. Вернадского,</strong
          >
          Балтийским федеральным университетом им. И. Канта, в рамках НИР “Создание
          аннотированных наборов данных золотого стандарта из надежных неструктурированных
          клинических источников с разработкой систем глубокого машинного обучения
          для поддержки клинических решений на их основе” под руководством профессора
          <strong class="text-violet-400">
            Двирского Александра Анатольевича.</strong
          >
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          Сервис предназначен для автоматического составления меню и подбора
          питания, позволяет принимать оптимальные индивидуально ориентированные
          решения по вопросам питания, диетологии и нутрициологии <strong
            class="text-violet-400">на курортах Крыма</strong
          > в соответствии санитарно-эпидемиологическим требованиям РФ.
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          Центр создан в рамках Программы стратегического академического
          лидерства <strong class="text-violet-400">«Приоритет 2030»</strong> и является
          многопрофильным центром реабилитации, восстановления и поддержания здоровья
          высококвалифицированными специалистами на основе передовых научных исследований
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 py-4 text-center relative
    before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700
    after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl">Хотите узнать больше?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Немного <span class="text-violet-400">информации</span> о себе
      </h3>
    </div>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="lato font-semibold text-4xl am:text-5xl md:text-6xl text-slate-500"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>
              {benefit.description}
            </p>
          </div>
        </div>
      {/each}
    </div>
    <h5 class="lato font-semibold text-center text-2xl sm:text-3xl">
      Почему именно <span class="lato text-violet-400">Я?</span>
    </h5>
    <div
      class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
    >
      <table class="bg-white text-slate-700 rounded text-center">
        <thead class="border-b border-solid border-slate-200">
          <tr>
            <th></th>
            <th class="whitespace-nowrap p-2 px-4">Кандидиат №1</th>
            <th class="whitespace-nowrap p-2 px-4">Кандидиат №2</th>
            <th class="whitespace-nowrap p-2 px-4">Кандидиат №3</th>
            <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8"
              >Я</th
            >
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm text-left whitespace-nowrap"
              >Увлечённость</td
            >
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm text-left whitespace-nowrap"
              >Критическое мышление</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr><tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm text-left whitespace-nowrap"
              >Коммуникабельность</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr><tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm text-left whitespace-nowrap"
              >Творчество</td
            >
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="mx-auto -mt-12 italic md:hidden opacity-50">
      <p>Прокрутите чтобы увидеть всё &rarr;</p>
    </div>
    <p class="mx-auto">
      Есть повод поработать <span class="text-violet-400">вместе!</span>
    </p>
  </section>
</main>
