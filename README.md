# ECS8060: AI Engineering - Course Website

Course website for **AI Engineering (ECS8060)** at Queen's University Belfast.

## Quick Start

### Prerequisites

- Ruby 2.7+ and Bundler
- Or just use GitHub Pages (no local setup needed)

### Local Development

```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve

# View at http://localhost:4000
```

### Deploy to GitHub Pages

1. Create a repository named `username.github.io` or `org.github.io/ecs8060`
2. Push this code to the repository
3. Enable GitHub Pages in repository settings
4. The site will be available at the configured URL


## Customisation

### Update Course Information

Edit `_config.yml`:

```yaml
course_code: "ECS8060"
course_name: "AI Engineering"
university: "Queen's University Belfast"
semester: "Summer 2025"
```

### Update Schedule

Edit `_data/schedule.yml` to add/modify lectures, deadlines, and events.

### Update Team

Edit `_data/team.yml` with actual team member information.

### Add Sponsors

Edit `_data/sponsors.yml` and add sponsor logos to `assets/images/sponsors/`.

### Add Lecture Notes

Create Markdown files in `notes/` following the template in `notes/lecture-01.md`.

### Add Slides

Place PDF slides in `slides/` and update the schedule to link to them.


## Acknowledgement

Claude code was harmed in the making of this website. Stylistic inspirations taken from Stanford's CS231n and CS224N.
