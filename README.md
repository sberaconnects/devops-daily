

---

## 📊 GitHub Actions Badge

You can add this badge to your `README.md` to show the status of the daily workflow:

```markdown
![Daily Folder](https://github.com/sberaconnects/devops-daily/actions/workflows/daily-folder.yml/badge.svg)
```

---

## 📬 Optional: Weekly Digest (Manual Setup)

You can generate a weekly digest with a custom script like this:

```bash
#!/bin/bash
# weekly-summary.sh

echo "# Weekly Summary: $(date +%Y-%m-%d)" > weekly-summary.md
find . -type f -name notes.md | sort | tail -n 7 | while read file; do
  echo -e "\n## $(dirname "$file")" >> weekly-summary.md
  cat "$file" >> weekly-summary.md
done
```

Run every Sunday and commit the output as `weekly-summary.md`.

---

## 🌐 Optional: Turn Repo into a GitHub Page

1. Go to your GitHub repo → Settings → Pages
2. Select the `main` branch and `/root` directory
3. Click **Save**

Your logs will be available at:
```
https://sberaconnects.github.io/devops-daily/
```

You can create a custom landing page in `index.md` or `docs/index.html`.

