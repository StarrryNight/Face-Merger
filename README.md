# 🎭 Face Merger - Party Game Edition

**What would your friends look like combined?** Find out with this hilarious face-blending tool! Perfect for parties, game nights, or just having fun with your crew.

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.5+-green)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0.10+-orange)

---

## 🎉 How It Works

This tool takes two face photos and morphs them together into one hilarious hybrid face! It uses AI-powered facial landmark detection to seamlessly blend features like eyes, noses, mouths, and more.

---

## 🚀 Quick Start

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Gather Your Party Photos

Take clear face photos of everyone at your party. For best results:
- ✅ Face the camera directly
- ✅ Good lighting (no harsh shadows)
- ✅ Neutral expression works best
- ✅ One face per photo

### 3. Add Photos to the `Faces` Folder

Save each person's photo as a `.png` file named after them:

```
Faces/
├── Alice.png
├── Bob.png
├── Charlie.png
├── Dana.png
└── ...
```

### 4. Create Your Blend Pairs

Edit `Faces.txt` to specify which faces to merge. Each line should have two names separated by a comma:

```
Alice, Bob
Charlie, Dana
Alice, Charlie
Bob, Dana
```

**💡 Pro tip:** For a party of N people, try blending everyone with everyone! That's N×(N-1)/2 unique combinations.

### 5. Run the Face Merger!

```bash
python batch_blend.py
```

Watch the magic happen! All blended faces will appear in the `Results` folder.

---

## 📂 Project Structure

```
Face-Merger/
├── Faces/              # Put your party photos here (.png files)
├── Results/            # Blended faces appear here
├── Faces.txt           # Define who gets blended with who
├── batch_blend.py      # Run this to blend all pairs
├── face_blender.py     # Core face morphing engine
└── requirements.txt    # Python dependencies
```

---

## 🎮 Party Game Ideas

### 1. **"Guess the Parents"**
Blend two friends together and have everyone guess which two people created the "baby"!

### 2. **"Celebrity Mashup"**
Add celebrity photos to the mix and see what your friends would look like combined with their favorite stars!

### 3. **"Speed Dating Results"**
At the end of the night, reveal what everyone's "couples photo" would look like if they merged faces!

### 4. **"Family Reunion"**
Blend siblings, parents, or couples to see whose features dominate!

---

## ⚙️ Advanced Usage

### Single Pair Mode

Blend just two specific images:

```bash
python face_blender.py person_a.jpg person_b.jpg -o result.jpg
```

### Custom Options

```bash
python face_blender.py image1.jpg image2.jpg -o output.jpg -s 800 -b 0.5
```

| Option | Description | Default |
|--------|-------------|---------|
| `-o` | Output filename | `blended_result.jpg` |
| `-s` | Output size (pixels) | `600` |
| `-b` | Blend ratio (0.0-1.0) | `0.5` |

A blend ratio of `0.5` means equal parts of both faces. Try `0.3` or `0.7` to weight toward one person!

---

## 🔧 Troubleshooting

| Problem | Solution |
|---------|----------|
| "No face detected" | Use a clearer photo with the face fully visible |
| Weird artifacts | Ensure both photos have similar lighting |
| Missing dependencies | Run `pip install -r requirements.txt` |
| "Image not found" | Check your filenames match exactly (case-sensitive!) |

---

## 📸 Tips for Best Results

1. **Consistent lighting** - Similar lighting in both photos = smoother blends
2. **Front-facing photos** - Profile shots don't work well
3. **Similar head sizes** - The tool will resize, but starting similar helps
4. **Clear, high-res images** - Blurry photos = blurry results

---

## 🎊 Have Fun!

Made with ❤️ for parties, pranks, and good times. Share your funniest blends!

---

## License

MIT License - Do whatever you want with it! Just have fun. 🎈
