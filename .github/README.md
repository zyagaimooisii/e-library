# bookmarkletの追加方法
追加しやすいようにリンクかしたものは[ここ](https://zyagaimooisii.github.io/e-library/)←なぜかうまく動かなくなるから↓のコードをコピーして適当なページをブックマークに登録してそれのリンクの部分をコードに書き換えてください
## open-AI-iframe.js

javascript:(function()%7Bvar%20questionText=document.querySelector('.qtext-container').textContent;var%20answerElements=document.querySelectorAll('%23questionanswer-01%20li');var%20answers=%5B%5D;for(var%20i=0;i%3CanswerElements.length;i++)%7Banswers.push(answerElements%5Bi%5D.textContent);%7Dvar%20question=questionText+'%5Cn%5Cn'+answers.join(',');var%20data=%7Bquestion:question%7D;var%20iframe=document.createElement('iframe');iframe.style.position='fixed';iframe.style.top=0;iframe.style.left=0;iframe.style.width='100%25';iframe.style.height='300px';iframe.src='https://loud-changeable-bestseller.glitch.me/?question='+encodeURIComponent(question);document.body.appendChild(iframe);%7D)();

## open-AI-iframe.jsの使い方
eライブラリの問題の画面を開きながらこのブックマークレットを実行すると、ページの左上にAIのサイトがiframeで表示されます。
何も押さなくても自動的に送信してくれるので返答が来るのを待ちましょう。
エラーが返ってきた場合は時間が経ってからもう一度やると正常に返ってくることがあります。3回やってもダメだったら大人しく諦めよう。
画像がある問題には使わないでね(適当な答えを返されます)計算問題もおかしくなることがあるから控えた方がいいです。
## Show-answer-explanation.js

javascript:(function()%7B%20%20%20var%20explainText%20=%20document.getElementById('explain-dialog').textContent;%20%20%20var%20h2Elements%20=%20document.getElementsByTagName('h2');%20%20%20%20for%20(var%20i%20=%200;%20i%20%3C%20h2Elements.length;%20i++)%20%7B%20%20%20%20%20var%20h2Element%20=%20h2Elements%5Bi%5D;%20%20%20%20%20var%20newParagraph%20=%20document.createElement('p');%20%20%20%20%20newParagraph.textContent%20=%20explainText;%20%20%20%20%20h2Element.parentNode.insertBefore(newParagraph,%20h2Element.nextSibling);%20%20%20%7D%20%7D)();

## Show-answer-explanation.jsの使い方
eライブラリの問題の画面を開きながらこのブックマークレットを実行すると、本来回答が終わった後にしか見ることのできない解答解説を見ることができます。
解答解説は問題文の上に表示されます。
※数学や理科の計算のところはLaTeXが使われているので正しく表示されません。(答えは頑張れば読み取れます)
## ai-answer-new.js
javascript:(function()%20%7B%0A%20%20var%20questionText%20=%20document.querySelector('.qtext-container').textContent;%0A%20%20var%20answerElements%20=%20document.querySelectorAll('%23questionanswer-01%20li');%0A%20%20var%20answers%20=%20%5B%5D;%0A%20%20for%20(var%20i%20=%200;%20i%20%3C%20answerElements.length;%20i++)%20%7B%0A%20%20%20%20answers.push(answerElements%5Bi%5D.textContent);%0A%20%20%7D%0A%0A%20%20var%20explainElement%20=%20document.getElementById('explain-dialog');%0A%20%20var%20explainText%20=%20explainElement%20?%20explainElement.textContent%20:%20'';%0A%0A%20%20var%20question%20=%20questionText%20+%20'%5Cn%5Cn'%20+%20answers.join(',')%20+%20'%5Cn%5Cn'%20+%20explainText;%0A%20%20var%20data%20=%20%7B%20question:%20question%20%7D;%0A%20%20var%20iframe%20=%20document.createElement('iframe');%0A%20%20iframe.style.position%20=%20'fixed';%0A%20%20iframe.style.top%20=%200;%0A%20%20iframe.style.left%20=%200;%0A%20%20iframe.style.width%20=%20'100%25';%0A%20%20iframe.style.height%20=%20'300px';%0A%20%20iframe.src%20=%20'https://loud-changeable-bestseller.glitch.me/?question='%20+%20encodeURIComponent(question);%0A%20%20document.body.appendChild(iframe);%0A%7D)();%0A
## ai-answer-new.jsの使い方
open-AI-iframe.jsのAIに送信する質問にShow-answer-explanation.jsで表示される解答解説を追加してAIの解答の精度を上げたもの

