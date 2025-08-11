<script>
  import { Button } from "$lib/components/ui/button";
  
  const plans = [
    {
      name: "Basic",
      price: "$35",
      duration: "per hour",
      features: [
        "One-on-one tutoring",
        "Subject specific help",
        "Homework assistance",
        "Weekly sessions",
        "Progress reports"
      ],
      highlighted: false
    },
    {
      name: "Standard",
      price: "$30",
      duration: "per hour",
      features: [
        "All Basic features",
        "Study materials included",
        "Practice tests",
        "Bi-weekly sessions",
        "Email support between sessions",
        "Customized learning plan"
      ],
      highlighted: true
    },
    {
      name: "Premium",
      price: "$25",
      duration: "per hour",
      features: [
        "All Standard features",
        "Unlimited email support",
        "Monthly progress meetings with parents",
        "College application assistance",
        "Standardized test prep",
        "Flexible scheduling"
      ],
      highlighted: false
    }
  ];
</script>

<div class="container mx-auto px-4 py-16 sm:px-6 lg:px-8">
  <div class="mx-auto max-w-5xl text-center text-slate-900">
    <h1 class="mb-4 text-4xl font-bold tracking-tight sm:text-5xl">Simple, Transparent Pricing</h1>
    <p class="mx-auto mb-16 max-w-2xl text-xl text-slate-700">
      Invest in your academic success with our affordable tutoring packages.
    </p>
    
    <div class="grid gap-8 lg:grid-cols-3">
      {#each plans as plan}
        <div class="flex flex-col rounded-lg {plan.highlighted ? 'border-2 border-purple-500 shadow-lg' : 'border border-slate-200 shadow-sm'} bg-white p-8">
          {#if plan.highlighted}
            <div class="-mt-10 mb-4">
              <span class="inline-block rounded-full bg-purple-100 px-4 py-1 text-sm font-medium text-purple-800">
                Most Popular
              </span>
            </div>
          {/if}
          
          <h3 class="mb-2 text-2xl font-bold">{plan.name}</h3>
          <div class="mb-6">
            <span class="text-4xl font-extrabold">{plan.price}</span>
            <span class="text-slate-600">/{plan.duration}</span>
          </div>
          
          <ul class="mb-8 space-y-3 text-left">
            {#each plan.features as feature}
              <li class="flex items-start">
                <svg class="mr-2 h-5 w-5 shrink-0 text-green-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"></path>
                  <polyline points="22 4 12 14.01 9 11.01"></polyline>
                </svg>
                <span>{feature}</span>
              </li>
            {/each}
          </ul>
          
          <div class="mt-auto">
            <Button variant={plan.highlighted ? "default" : "outline"} class="w-full">
              Choose {plan.name}
            </Button>
          </div>
        </div>
      {/each}
    </div>
    
    <p class="mt-12 text-center text-lg text-slate-600">
      Need a custom plan? <Button variant="link" class="p-0 text-lg font-medium">Contact us</Button>
    </p>
  </div>
</div>
