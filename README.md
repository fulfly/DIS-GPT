# DIS-GPT

**DIS‑GPT** is an AI-powered assistant for automated, structured analysis of drug disintegration. Instead of relying on manual annotation, it leverages a curated pharmaceutical knowledge base to describe drug behavior across eight critical dimensions.

> 🌐 **Try online**: [https://chatgpt.com/g/g-6858fd80c7e4819193f0f1096dd7c05a-disgpt-test](https://chatgpt.com/g/g-6858fd80c7e4819193f0f1096dd7c05a-disgpt-test)

---

## 📂 Project Overview

This repository contains structured prompt instructions and `.json` knowledge files for large language models (LLMs) to describe drug disintegration processes across the following eight dimensions:

- `color_change`
- `shape_change`
- `surface_texture_change`
- `volume_change`
- `dissolution_speed_and_time`
- `physical_state_change`
- `dissolution_medium`
- `fragment_distribution_with_density`

All files are located in the `LLM describe/` directory.

---

## ⚡ How to Use

1. Open the web tool:  
   👉 [DIS‑GPT ChatGPT Plugin](https://chatgpt.com/g/g-6858fd80c7e4819193f0f1096dd7c05a-disgpt-test)

2. Use the following prompts in sequence to guide the model:

---

## 🧠 Prompt Guide

### ① Task Description Prompt

```

I need you to try analyzing the disintegration images of two groups of drugs, A and B. These may be images of the same drug or different drugs. I need you to determine whether the images are from the same drug or not. For each group, I will upload five images, each picture is taken 6 hours apart. Please describe the drug disintegration process in English for each image in the group, and finally, determine whether the two sets of images are from the same drug.

```

---

### ② Call the Knowledge Base

```

You can call the Knowledge Base to remember how to describe the drug disintegration. As you describe the tablets in English, pay attention to the changes in the size and shape of the tablets. If you have prepared, then I will upload the picture of group A pic1 of 0 hours.

```

**If not successfully loaded:**

```

You are not prepared totally. Please call the Knowledge Base to remember how to describe the drug disintegration again.

```

---

### ③ Per-Image Description Prompt

```

When you describe the drug, I hope you can make sure your description in English is accurate, think more, and reduce the occurrence of hallucinations. Each picture is taken 6 hours apart. It is group A/B pic N.

```

---

### ④ Comparison & Final Conclusion

```

Please compare Groups A and B based on their disintegration characteristics across the eight dimensions to determine if they are from the same drug or not. And explain why you think so.

```

---

## 📁 Repository Structure

```

LLM describe/
├── drug\_disintegration\_color\_change.json
├── drug\_disintegration\_dissolution\_medium.json
├── drug\_disintegration\_dissolution\_speed\_and\_time.json
├── drug\_disintegration\_fragment\_distribution\_with\_density.json
├── drug\_disintegration\_physical\_state\_change.json
├── drug\_disintegration\_shape\_change.json
├── drug\_disintegration\_surface\_texture\_change.json
├── drug\_disintegration\_volume\_change.json
├── drug\_disintegration\_introduction.json
├── drug\_disintegration\_summary.json
├── drug\_identification guide.json
├── Comprehensive Guide to Describing Drug Disintegration Images.pdf

```

---

## 📝 License

This repository is intended for academic and research use only.

---

## 🙏 Acknowledgments

Thanks to the Fu groupand contributors for curating the JSON knowledge modules. This work is part of a broader effort to integrate LLMs into pharmaceutical analysis pipelines.
```

