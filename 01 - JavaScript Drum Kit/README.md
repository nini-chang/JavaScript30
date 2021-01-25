## 01 - JavaScript Drum Kit

### 操作
- 按下相對應的英文字母按鍵，就會聽到聲音

### 筆記
1. `data-*` attribute(屬性)：一種自定義屬性的方法，不可包含大寫。每個人的命名會有所不同，如果直接搜尋不一定會有結果且不一定有相同意義，而這邊練習使用 `data-key` 並賦予 keyCode 的值，綁定按鍵(key)與聲音(audio)。參考 [MDN Using data attributes](https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes)

> keycode 可查詢[此連結](https://keycode.info/)

2. `window.addEventListener(eventName, eventHandler, eventPhase)`: 使整個網頁(window)監聽事件。
   - eventName: string, 事件名稱：keydown, click...
   - eventHandler: function, 進行哪些操作寫在這邊
   - eventPhase: boolean, 可以參考[這篇文章](https://blog.techbridge.cc/2017/07/15/javascript-event-propagation/)
   - 本次練習：按下按鍵則發出按鍵所對應的聲音
   ```
   window.addEventListener('keydown', function(e) {});

   // 也可以寫成 arrow function
   window.addEventListener('keydown', (e) => {})
   ```

3. `audio.currentTime = 0`: 將音檔時間設回 0。本次練習希望可以達到使用者每次按壓按鍵都會即時發出聲響，就必須將音檔時間設定至每次點擊後回到 0，才有辦法達到使用者下一次按壓按鍵時即時發出聲響的效果。請參考[這篇文章](https://www.codespeedy.com/set-audio-playing-time-to-starting-position-in-javascript/)
