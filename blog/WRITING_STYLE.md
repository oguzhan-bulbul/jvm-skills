# Technical Blog Writing Style

Use this when drafting or editing technical blog posts for `tschuehly.de`.

## Voice & Tone

### Perspective

- Use first person plural (`we`) when guiding readers through steps.
- Use first person singular (`I`) for personal preferences: `I personally use...`, `I prefer...`, `I recommend...`.
- Keep the tone direct and conversational, never academic or stiff.

### Personality

- Be opinionated and concrete.
- Use a bit of humor when it helps.
- Reference familiar developer pain points, especially JavaScript complexity.
- Mention personal tool preferences when relevant and real.

### Common Expressions

- `Let's first...` when starting a section
- `If you want to learn more...` when linking related resources
- `ping me on twitter` for questions, when appropriate

## Article Structure

### Opening Patterns

Start with one of:

1. A hook statement introducing a tool or concept with benefits
2. A problem statement about current pain points
3. A rhetorical question challenging the status quo

Example:

`We build the web frontend with a JavaScript framework, but why?`

### Section Hierarchy

- Use `#` for major sections.
- Use `##` for subsections.
- Use `###` for specific tasks or checkpoints.

### Checkpoints

For tutorials, include checkpoints to verify progress:

```markdown
### Checkpoint 1

![description](image.png)

If you click on that URL, you should see a "Hello World" in your browser.
```

### Article Closing

Close with:

1. A short summary of what was accomplished
2. Links to related content or series
3. Relevant self-promotion only when it fits naturally

## Code Formatting

### Code Blocks

Include file paths where useful.

Java:

```java
// path/to/File.java
package com.example;

@Controller
public class HelloController {
}
```

Templates:

```xml
<!-- TemplateName.jte -->
@param SomeContext context
<div>${context.value()}</div>
```

YAML:

```yaml
# path/to/application.yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost/db
```

Shell:

```bash
cd ./project
./mvnw spring-boot:run
```

### Inline Code

Use backticks for file names, class names, methods, annotations, commands, variables, and endpoints.

## Explanations

### "In detail:" Pattern

After code, explain with arrow notation:

```markdown
In detail:

- `@PreAuthorize("hasRole('ADMIN')")` -> checks the user has authority `ROLE_ADMIN`
- `@RestController` -> creates a Spring controller bean
- The `registration:` block defines OAuth2 client credentials
```

### Callouts

Use blockquotes for tips and important notes:

```markdown
> I recommend using constants for URL endpoints because you can navigate with ctrl+b in IntelliJ.
```

### External Quotes

```markdown
> ViewComponents consolidate the logic needed for a template into a single class
>
> [https://viewcomponent.org/#single-responsibility](https://viewcomponent.org/#single-responsibility)
```

## Visual Elements

### Images

- Keep cover images next to the markdown file in `posts/<category>/`.
- Reference them in frontmatter with `coverImage: filename.png`.
- Use standard markdown for inline images: `![alt text](image.png)`.

### Feature Lists

Use plain bullet lists:

```markdown
Some of the features that are really nice:

* Continuous deployment using GitHub
* System Monitoring
* Paketo Buildpack support
```

## Links & References

### Link Patterns

- Prefer official documentation for external references.
- Link related posts and series when helpful.
- Use direct links for talks and recordings.

### Affiliate Links

Only include them when they add real value and the recommendation is genuine.

## Technical Conventions

### Spring ViewComponent

When explaining ViewComponent:

1. Show the Java component class with `@ViewComponent`
2. Show the corresponding template
3. Show controller usage with `render()`
4. Explain the component lifecycle

### htmx

Cover both sides:

- Template usage like `hx-get`, `hx-target`, `hx-post`
- Server responses like `HX-Retarget`, `HX-Reswap`, `HX-Trigger`

### Constants

Emphasize maintainability and navigability:

```markdown
As you can see we are using static constants heavily, to make it easy to understand what controller mappings htmx sends requests to.
```

## Content Focus Areas

Primary topics:

- Spring Boot server-side rendering
- htmx for interactivity
- JTE templating
- Spring ViewComponent
- Deployment with Dokploy, Koyeb, or Hetzner
- Spring Security and authorization

Frame these as practical solutions to JavaScript complexity and full-stack Spring development.
