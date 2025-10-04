---
layout: page
title: 🤖 Hallucination Reduction
permalink: /hallucination_reduction/
description: Steering and trianing LLMs to hallucinate less!
img: assets/img/project_casal/casal.png
#redirect: https://unsplash.com
importance: 1
category: AI
---


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cite - CASAL</title>
    <style>
        .citation-box {
            background: #f7fafc;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            padding: 20px;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            line-height: 1.6;
            color: #2d3748;
            white-space: pre-wrap;
            word-wrap: break-word;
            margin-bottom: 20px;
        }

        .copy-button {
            background: #9333ea;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .copy-button:hover {
            background: #7e22ce;
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(147, 51, 234, 0.4);
        }

        .copy-button:active {
            transform: translateY(0);
        }

        .copy-button.copied {
            background: #48bb78;
        }
    </style>
</head>
<body>
    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
        <h2 style="margin: 0;">Cite This Work</h2>
        
        <button class="copy-button" onclick="copyToClipboard()">
            <span id="buttonText">Copy to Clipboard</span>
        </button>
    </div>
    
    <div class="citation-box" id="citation">@article{yang2025casal,
  title={Hallucination Reduction with CASAL: Contrastive Activation Steering for Amortized Learning},
  author={Yang, Wannan and Qiu, Xinchi and Yu, Lei and Zhang, Yuchen and Yang, Oliver Aobo and Kokhlikyan, Narine and Cancedda, Nicola and Garcia-Olano, Diego},
  journal={preprint},
  year={2025}
}</div>
    
    <div style="display: flex; justify-content: flex-end; margin-bottom: 20px;">
        <a href="/assets/pdf/CASAL_META.pdf" download="CASAL_META.pdf" class="copy-button" style="text-decoration: none;">
            Download PDF
        </a>
    </div>

    <script>
        function copyToClipboard() {
            const citation = document.getElementById('citation').textContent;
            const button = document.querySelector('.copy-button');
            const buttonText = document.getElementById('buttonText');
            
            navigator.clipboard.writeText(citation).then(() => {
                button.classList.add('copied');
                buttonText.textContent = 'Copied!';
                
                setTimeout(() => {
                    button.classList.remove('copied');
                    buttonText.textContent = 'Copy to Clipboard';
                }, 2000);
            }).catch(err => {
                console.error('Failed to copy:', err);
            });
        }
    </script>
</body>
</html>

<object data="/assets/pdf/CASAL_META.pdf" width="1000" height="1000" type='application/pdf'></object>