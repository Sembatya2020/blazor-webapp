# BlazorApp1 — Exercise changes

This workspace contains a sample Blazor app used for exercises on creating and modifying components.

What I added/changed

- `Components/Pages/Counter.razor`
  - Added a `[Parameter] public int IncrementAmount { get; set; } = 1;` property.
  - `IncrementCount` now increases `currentCount` by `IncrementAmount`.

- `Components/Pages/Home.razor`
  - Updated to use the Counter component with `IncrementAmount="10"`:
    `<Counter IncrementAmount="10" />`
  - This makes the Home page counter increment by 10 per click.

- `Pages/PizzaBrowser.razor`
  - New simple demo UI showing a few pizzas with an "Add to cart" button.
  - Demonstrates dynamic rendering and event handling in a Blazor component.

How to run (PowerShell)

```powershell
cd C:\Users\DELL\Desktop\.net\blazor-webapp
# Run the Blazor project
dotnet run --project .\BlazorApp1\BlazorApp1.csproj

# Or use hot reload during development:
# dotnet watch run --project .\BlazorApp1\BlazorApp1.csproj
```

Open the URL shown by the running app (for example `https://localhost:7161`) and:
- Visit `/` to see the Home page (Counter increments by 10 on Home).
- Visit `/counter` to see the Counter page (increments by 1 by default).
- Visit `/pizzabrowser` to see the sample PizzaBrowser component.

Notes

- The pizza component is a small demo scaffold — extend it with real data or navigation as needed.
