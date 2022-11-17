# Bridge toaster

An elegant and simple notification for javascript, with no dependencies


Features
--------

+ Simple CSS-animated customizable toast pop-ups for any design
+ No dependencies and `< 1kb` code
+ Toasts appear and disappear by specifying optional timeout


Installation & Usage
--------------------

bridge-toaster is primarily ES6 module. See it in action:

```bash
npm i bridge-toaster
```

```javascript
import bridgeToaster from "bridge-toaster"

bridgeToaster('success', 'Hello Toaster!')
```

Parameters:
```javascript
bridgeToaster(
  'error',    // Toaster style type. Pre-defined: error, warning or success
  'message',  // Message
  false       // Timeout in ms (default: 5000)
)

```

Parameters:
```css

#bridge-toaster .toast {
  z-index: 9999;
  padding: 20px;
  width: 100%;
  max-width: 300px;
  position: fixed;
  bottom: 0px;
  left: 10px;
  color: white;
  transition: 0.3s;
  transform: translateY(0);
  opacity: 0;
  font-size: 12px;
  background: rgba(35, 37, 43, 0.9);
}

#bridge-toaster .toast.error {
  background: rgba(139, 0, 0, 0.9);
}

#bridge-toaster .toast.warning {
  background: rgba(255, 140, 0, 0.9);
}

#bridge-toaster .toast.success {
  background: rgba(60, 188, 75, 0.9);
}

#bridge-toaster .toast.active {
  opacity: 1;
  bottom: 10px;
}

@media (max-width: 568px) {
  #bridge-toaster .toast {
    max-width: none;
    width: calc(100% - 40px);
    margin: auto;
    left: 0;
    right: 0;
  }
}

```

Import the style

```javascript
@import ~bridge-toaster/src/bridge-toaster // or '~bridge-toaster/dist/bridge-toaster.min.css'
```
