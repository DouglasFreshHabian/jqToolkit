
<p align="center">
  <img src="https://github.com/DouglasFreshHabian/jqToolkit/blob/main/Assets/Tux-Json.png?raw=true" alt="My Image" width="400">
</p>

<h1 align="center">
{🔨} jqToolkit
	</h1>


## 🛠️ Requirements: jq
The Swiss Army Knife of JSON in the Terminal.
```bash
sudo apt install jq
```
 ---

## 💡 Commands:
Be sure to grab the provided `sample_data.json` file to practice with!

### 🧪 1 – Pretty Print (Clean Display)

```bash
cat sample_data.json | jq
```

> *Boom.* Clean, color-coded JSON in one keypress.

---

### 🧪 2 – Run a Simple Command:

```bash
jq '.users[] | select(.active == true)' sample_data.json
```

> Need a field? Just call it.

---

### 🧪 3 – Extract emails of admins:

```bash
jq -r '.users[] | select(.admin == true) | .email' sample_data.json
```

---

### 🧪 4 – Get usernames from US users:

```bash
jq -r '.users[] | select(.country == "US") | .username' sample_data.json
```

---

### 🧪 5 – Parse API Output

```bash
curl -s https://api.github.com/users/octocat | jq '.public_repos'
```

> Live API. No browser. No bullshit.

---

### 🧪 6 - Check Video Metadata for Analysis

```bash
yt-dlp -j https://youtu.be/your-video-id | jq
```
> This only works if `yt-dlp` is installed on your system.
