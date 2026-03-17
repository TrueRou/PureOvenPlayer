# PureOvenPlayer

OvenPlayer simple wrapper for customizing the player and adding features. It is not a fork of OvenPlayer, but a separate project that uses OvenPlayer as a dependency. It is designed to be easy to use and customize, and to provide a simple configuration interface for adding features and customizing the player.

## Usage

Simply download the html file and deploy or distribute it. You can customize the player by editing the configuration object in the script tag.

## Configuration

```javascript
window.PlayerConfig = {
  player: {
    autoStart: true,
    autoFallback: false,
    defaultSourceIndex: 0,
    sources: [
      {
        type: 'webrtc',
        file: '{wsProtocol}//demo.ovenplayer.com{signallingPort}/app/stream?transport=tcp',
        label: 'WebRTC/TCP'
      },
      {
        type: 'webrtc',
        file: '{wsProtocol}//demo.ovenplayer.com{signallingPort}/app/stream',
        label: 'WebRTC'
      },
      {
        type: 'hls',
        file: '{httpProtocol}//demo.ovenplayer.com{httpStreamingPort}/app/stream/llhls.m3u8',
        label: 'LL-HLS'
      }
    ]
  },
  theme: {
    pageBackground: {
      color: '#eef3ff',
      image: '',
      gradient: 'linear-gradient(120deg, #eef3ff 0%, #ffffff 45%, #f4f8ff 100%)',
      size: 'cover',
      position: 'center center',
      repeat: 'no-repeat'
    },
    sourceButton: {
      activeBackground: '#0d6efd',
      activeColor: '#ffffff',
      inactiveBackground: '#ffffff',
      inactiveColor: '#0d6efd',
      borderColor: '#0d6efd'
    },
    brand: {
      text: 'OVENPLAYER',
      href: '/',
      color: '#1f2937'
    }
  }
};
```