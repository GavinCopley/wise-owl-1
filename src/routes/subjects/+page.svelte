<script>
  import { Button } from "$lib/components/ui/button";
  
  const subjects = [
    {
      name: "Mathematics",
      description: "From elementary arithmetic to advanced calculus, our math tutors help students build strong foundations and tackle complex problems with confidence.",
      levels: ["Elementary", "Middle School", "High School", "College"]
    },
    {
      name: "Science",
      description: "Our science tutoring covers biology, chemistry, physics, and earth sciences with an emphasis on conceptual understanding and practical applications.",
      levels: ["Elementary", "Middle School", "High School", "College"]
    },
    {
      name: "English",
      description: "From reading comprehension to essay writing, our English tutors help students improve their language skills and develop a love for literature.",
      levels: ["Elementary", "Middle School", "High School", "College"]
    },
    {
      name: "History",
      description: "Our history tutors bring the past to life, helping students understand historical events, their contexts, and their relevance to the present day.",
      levels: ["Middle School", "High School", "College"]
    }
  ];
</script>

<div class="container mx-auto px-4 py-16 sm:px-6 lg:px-8">
  <div class="mx-auto max-w-4xl text-slate-900">
    <h1 class="mb-2 text-4xl font-bold tracking-tight sm:text-5xl">Subjects We Teach</h1>
    <p class="mb-12 text-xl text-slate-700">Comprehensive tutoring across a wide range of academic disciplines</p>
    
    <div class="grid gap-8 md:grid-cols-2">
      {#each subjects as subject}
        <div class="rounded-lg border border-slate-200 bg-white p-6 shadow-sm">
          <h2 class="mb-3 text-2xl font-semibold text-slate-900">{subject.name}</h2>
          <p class="mb-4 text-slate-700">{subject.description}</p>
          <div class="mb-4 flex flex-wrap gap-2">
            {#each subject.levels as level}
              <span class="inline-flex items-center rounded-full bg-purple-100 px-3 py-1 text-xs font-medium text-purple-800">
                {level}
              </span>
            {/each}
          </div>
          <Button variant="outline" class="mt-2 w-full">Learn More</Button>
        </div>
      {/each}
    </div>
    
    <div class="mt-12 text-center">
      <p class="mb-6 text-lg text-slate-700">Don't see the subject you need help with?</p>
      <Button variant="default">Contact Us</Button>
    </div>
  </div>
</div>
