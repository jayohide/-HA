kiosk_mode: null  
  hide_header: true
  hide_sidebar: true
views:
  - theme: Backend-selected
    title: Plan
    path: plan
    icon: mdi:floor-plan
    type: panel
    badges: []
    cards:
      - type: custom:config-template-card
        entities:
          - light.mbulb3_cloud_217376
          - light.dengdai
          - light.mbulb3_cloud_216068
        card:
          type: picture-elements
          image: /local/UI/关灯背景.png
          elements:
            - type: image
              entity: light.mbulb3_cloud_217376
              tap_action:
                action: none
              style:
                pointer-events: none
                top: 50%
                left: 50%
                width: 100%
                mix-blend-mode: lighten
              state_image:
                'off': /local/UI/transparent.png
                'on': /local/UI/客厅开灯.png
            - type: image
              entity: light.mbulb3_cloud_217376
              tap_action:
                action: toggle
              style:
                top: 45%
                left: 70.6%
                width: 7%
              state_image:
                'off': /local/UI/light_off.png
                'on': /local/UI/light_on.png
            - type: image
              entity: light.mbulb3_cloud_216068
              tap_action:
                action: none
              style:
                pointer-events: none
                top: 50%
                left: 50%
                width: 100%
                mix-blend-mode: lighten
              state_image:
                'off': /local/UI/transparent.png
                'on': /local/UI/卧室开灯.png
            - type: image
              entity: light.mbulb3_cloud_216068
              tap_action:
                action: toggle
              style:
                top: 35.6%
                left: 39.5%
                width: 7%
              state_image:
                'off': /local/UI/light_off.png
                'on': /local/UI/light_on.png
            - type: image
              entity: light.dengdai
              tap_action:
                action: none
              style:
                pointer-events: none
                top: 50%
                left: 50%
                width: 100%
                mix-blend-mode: lighten
              state_image:
                'off': /local/UI/transparent.png
                'on': /local/UI/次卧开灯.png
            - type: image
              entity: light.dengdai
              tap_action:
                action: toggle
              style:
                top: 40%
                left: 55%
                width: 7%
              state_image:
                'off': /local/ui/light_off.png
                'on': /local/ui/light_on.png
            - action: none
              image: /local/UI/3.楼层/on/1L.png
              style:
                left: 35.3%
                top: 8.6%
                width: 6.8%
              tap_action:
                action: navigate
                navigation_path: /lovelace-1/plan
              hold_action:
                action: none
              type: image
            - action: none
              entity: person.jenny
              state_image:
                home: /local/UI/1.头像/在家.png
                not_home: /local/UI/1.头像/不在家.png
              style:
                background-color: rgba(255, 255, 255, 0.0)
                border-radius: 55%
                height: 9.8%
                left: 8.9%
                top: 72%
                width: 7%
              tap_action: none
              type: image
            - action: none
              entity: person.jason
              state_image:
                home: /local/UI/1.头像/在家-J.png
                not_home: /local/UI/1.头像/不在家-J.png
              style:
                background-color: rgba(255, 255, 255, 0.0)
                border-radius: 55%
                height: 9.8%
                left: 18.5%
                top: 72%
                width: 7%
              tap_action: none
              type: image
            - action: none
              image: /local/UI/2.侧边栏/ON/1-家庭总览.png
              style:
                left: 13.9%
                top: 33.2%
                width: 17.6%
              tap_action:
                action: navigate
                navigation_path: /dashboard-home/light
              hold_action:
                action: none
              type: image
            - action: none
              image: /local/UI/2.侧边栏/OFF/2-所有设备.png
              style:
                left: 13.9%
                top: 42.2%
                width: 17.6%
              tap_action:
                action: navigate
                navigation_path: /dashboard-home/light
              hold_action:
                action: none
              type: image
            - action: none
              image: /local/UI/2.侧边栏/OFF/3-媒体控制.png
              style:
                left: 13.9%
                top: 51.2%
                width: 17.6%
              tap_action:
                action: navigate
                navigation_path: /lovelace-jason/media
              hold_action:
                action: none
              type: image
            - action: none
              image: /local/UI/2.侧边栏/OFF/4-扫地机器人 .png
              style:
                left: 13.9%
                top: 60.2%
                width: 17.6%
              tap_action:
                action: navigate
                navigation_path: /lovelace-jason/robot
              hold_action:
                action: none
              type: image
            - color_thresholds:
                - color: '#4dd2ff'
                  value: 17
                - color: '#01a4db'
                  value: 20
                - color: '#fccd68'
                  value: 26
                - color: '#ff1a1a'
                  value: 30
              entities:
                - sensor.temperature
              icon: mdi:home-thermometer-outline
              update_interval: 600
              show:
                icon: true
                legend: false
                name: false
              style: |
                :host {
                 left: 14%;
                 top:  88.6%;
                 width: 22.4%;
                 overflow: hidden;
                 height: 15%;
                 background: none  !important;
                 box-shadow: none !important;
                }
                .header {
                 font-size: 100%;
                 position: absolute !important;
                 width: 5% !important;
                 padding: 1% !important;
                 right: 20% !important;
                 top: 15% !important;
                }
                ha-card {
                 background: none  !important;
                 padding: 0 !important;
                }
                .icon > ha-icon {
                 width:30% !important;
                 height:100% !important;
                }
                .state__time{
                 font-size:1vw !important;
                 margin-top: 0.2vw;
                 font-weight: 300 !important;
                 opacity: 0.6 !important;
                }
                .states {
                 font-size: 80% !important;
                 padding: 1vw 0vw 0vw 0vw  !important;
                 margin: auto !important;
                 width: 70%;
                }
              tap_action:
                action: navigate
                navigation_path: /lovelace-jason/weather
              type: custom:mini-graph-card
            - backdrop: false
              entity: weather.chengdu
              name: ' '
              style: |
                :host {
                 left: 14%;
                 top:  18%;
                 width: 22.5%;
                 height: 2%;
                 overflow: ;
                 height: 2%;
                 background: none;
                 box-shadow: none;
                 font-size: 80%
                 }
                 ha-card {
                 background: none;
                 box-shadow: none;
                 flex-flow: none;
                 padding: 100;
                 }
              tap_action:
                action: navigate
                navigation_path: /lovelace-jason/weather
              type: custom:simple-weather-card
            - entity: sensor.date
              hold_action:
                action: none
              style:
                color: rgba(255, 255, 255, 0.5)
                font-size: 1.5vw
                font-weight: 300
                left: 19%
                letter-spacing: 0.24vw
                text-align: left
                top: 11%
                width: 30%
              tap_action:
                action: none
              type: state-label
            - entity: sensor.time
              hold_action:
                action: none
              style:
                color: rgba(121, 231, 255, 0.7)
                font-size: 430%
                font-weight: 400
                left: 3.5%
                letter-spacing: '-0.05vw'
                max-width: 1px
                top: 17%
              tap_action:
                action: none
              type: state-label
            - name: 后花园监控
              type: custom:mushroom-entity-card
              entity: camera.dsm_jason_de_iphone_xs_max
              icon_image: mdi:cctv
              style:
                left: 102.5%
                top: 91%
                width: 50%
                background: none
                font_color: rgba(255, 255, 255, 0.0)
            - name: 正门监控
              type: custom:mushroom-entity-card
              entity: camera.dsm_jason_de_iphone_xs_max
              icon_image: mdi:cctv
              style:
                left: 88%
                top: 91%
                width: 50%
                background: none
                font_color: rgba(255, 255, 255, 0.0)
            - name: 电脑桌监控
              type: custom:mushroom-entity-card
              entity: camera.dsm_jason_de_iphone_xs_max
              icon_image: mdi:cctv
              style:
                left: 54%
                top: 91%
                width: 50%
                background: none
                font_color: rgba(255, 255, 255, 0.0)
            - name: 猫咪监控
              type: custom:mushroom-entity-card
              entity: camera.dsm_jason_de_iphone_xs_max
              icon_image: mdi:cctv
              style:
                left: 70%
                top: 91%
                width: 50%
                background: none
                font_color: rgba(255, 255, 255, 0.0)
  - theme: Backend-selected
    title: 所有设备
    path: light
    icon: mdi:cellphone-link
    type: panel
    badges: []
    cards:
      - type: picture-elements
        image: /local/UI/所有设备背景.png
        elements:
          - enableColumns: true
            rows:
              - columns:
                  - column: 1
                    entities:
                      - entities:
                          - entity: light.mbulb3_cloud_217376
                            icon: mdi:ceiling-light
                          - entity: remote.apple_tv4k
                            icon: mdi:monitor
                          - entity: media_player.sony
                            icon: mdi:monitor
                          - entity: vacuum.sao_di_ji_qi_ren
                            icon: mdi:robot
                        title: 客厅
                    tileOnRow: 2
                  - column: 1
                    entities:
                      - entities:
                          - entity: light.dengdai
                            icon: mdi:ceiling-light
                          - entity: light.mbulb3_cloud_216068
                            icon: mdi:ceiling-light
                          - entity: media_player.redmi
                            icon: mdi:robot
                            name: 红米智能音箱
                          - entity: sensor.aqara
                            icon: mdi:robot
                            name: 人体传感器
                        title: 卧室
                    tileOnRow: 3
                  - column: 4
                    entities:
                      - entities:
                          - entity: button.dsm_shutdown
                            icon: mdi:close-circle-outline
                            name: DSM关机
                          - entity: button.dsm_reboot
                            icon: mdi:refresh
                            name: DSM重启
                        title: 网络设备
                    tileOnRow: 3
            statePositionTop: true
            style:
              height: 100%
              left: 68%
              top: 52%
              width: 85%
            type: custom:homekit-card
          - action: none
            entity: person.jenny
            state_image:
              home: /local/UI/1.头像/在家.png
              not_home: /local/UI/1.头像/不在家.png
            style:
              background-color: rgba(255, 255, 255, 0.0)
              border-radius: 55%
              height: 9.8%
              left: 8.9%
              top: 72%
              width: 7%
            tap_action: none
            type: image
          - action: none
            entity: person.jason
            state_image:
              home: /local/UI/1.头像/在家-J.png
              not_home: /local/UI/1.头像/不在家-J.png
            style:
              background-color: rgba(255, 255, 255, 0.0)
              border-radius: 55%
              height: 9.8%
              left: 18.5%
              top: 72%
              width: 7%
            tap_action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/ON/1-家庭总览.png
            style:
              left: 13.9%
              top: 33.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/plan
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/2-所有设备.png
            style:
              left: 13.9%
              top: 42.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/light
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/3-媒体控制.png
            style:
              left: 13.9%
              top: 51.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/media
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/4-扫地机器人 .png
            style:
              left: 13.9%
              top: 60.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/robot
            hold_action:
              action: none
            type: image
          - color_thresholds:
              - color: '#4dd2ff'
                value: 17
              - color: '#01a4db'
                value: 20
              - color: '#fccd68'
                value: 26
              - color: '#ff1a1a'
                value: 30
            entities:
              - sensor.temperature
            icon: mdi:home-thermometer-outline
            update_interval: 600
            show:
              icon: true
              legend: false
              name: false
            style: |
              :host {
               left: 14%;
               top:  88.6%;
               width: 22.4%;
               overflow: hidden;
               height: 15%;
               background: none  !important;
               box-shadow: none !important;
              }
              .header {
               font-size: 100%;
               position: absolute !important;
               width: 5% !important;
               padding: 1% !important;
               right: 20% !important;
               top: 15% !important;
              }
              ha-card {
               background: none  !important;
               padding: 0 !important;
              }
              .icon > ha-icon {
               width:30% !important;
               height:100% !important;
              }
              .state__time{
               font-size:1vw !important;
               margin-top: 0.2vw;
               font-weight: 300 !important;
               opacity: 0.6 !important;
              }
              .states {
               font-size: 80% !important;
               padding: 1vw 0vw 0vw 0vw  !important;
               margin: auto !important;
               width: 70%;
              }
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/weather
            type: custom:mini-graph-card
          - backdrop: false
            entity: weather.chengdu
            name: ' '
            style: |
              :host {
               left: 14%;
               top:  18%;
               width: 22.5%;
               height: 2%;
               overflow: ;
               height: 2%;
               background: none;
               box-shadow: none;
               font-size: 80%
               }
               ha-card {
               background: none;
               box-shadow: none;
               flex-flow: none;
               padding: 100;
               }
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/weather
            type: custom:simple-weather-card
          - entity: sensor.date
            hold_action:
              action: none
            style:
              color: rgba(255, 255, 255, 0.5)
              font-size: 1.5vw
              font-weight: 100
              left: 19%
              letter-spacing: 0.24vw
              text-align: left
              top: 11%
              width: 30%
            tap_action:
              action: none
            type: state-label
          - entity: sensor.time
            hold_action:
              action: none
            style:
              color: rgba(121, 231, 255, 0.7)
              font-size: 430%
              font-weight: 100
              left: 3.5%
              letter-spacing: '-0.05vw'
              max-width: 1px
              top: 17%
            tap_action:
              action: none
            type: state-label
  - theme: Backend-selected
    title: 扫地机
    path: robot
    icon: mdi:robot-vacuum
    type: panel
    badges: []
    cards:
      - type: picture-elements
        image: /local/UI/纯背景.png
        elements:
          - type: custom:xiaomi-vacuum-map-card
            entity: vacuum.sao_di_ji_qi_ren
            map_source:
              camera: camera.xiaomi_cloud_map_extractor
            calibration_source:
              camera: true
            vacuum_platform: default
            language: zh
            map_modes:
              - template: vacuum_clean_zone
            style: |
              :host {
                left: 62%;
                top:  60%;
                width: 50%;
                overflow: none;
                height: 100%;
                background: none;
                box-shadow: none;
          - action: none
            entity: person.jenny
            state_image:
              home: /local/UI/1.头像/在家.png
              not_home: /local/UI/1.头像/不在家.png
            style:
              background-color: rgba(255, 255, 255, 0.0)
              border-radius: 55%
              height: 9.8%
              left: 8.9%
              top: 72%
              width: 7%
            tap_action: none
            type: image
          - action: none
            entity: person.jason
            state_image:
              home: /local/UI/1.头像/在家-J.png
              not_home: /local/UI/1.头像/不在家-J.png
            style:
              background-color: rgba(255, 255, 255, 0.0)
              border-radius: 55%
              height: 9.8%
              left: 18.5%
              top: 72%
              width: 7%
            tap_action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/ON/1-家庭总览.png
            style:
              left: 13.9%
              top: 33.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/plan
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/2-所有设备.png
            style:
              left: 13.9%
              top: 42.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/light
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/3-媒体控制.png
            style:
              left: 13.9%
              top: 51.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/media
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/4-扫地机器人 .png
            style:
              left: 13.9%
              top: 60.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/robot
            hold_action:
              action: none
            type: image
          - color_thresholds:
              - color: '#4dd2ff'
                value: 17
              - color: '#01a4db'
                value: 20
              - color: '#fccd68'
                value: 26
              - color: '#ff1a1a'
                value: 30
            entities:
              - sensor.temperature
            icon: mdi:home-thermometer-outline
            update_interval: 600
            show:
              icon: true
              legend: false
              name: false
            style: |
              :host {
               left: 14%;
               top:  88.6%;
               width: 22.4%;
               overflow: hidden;
               height: 15%;
               background: none  !important;
               box-shadow: none !important;
              }
              .header {
               font-size: 100%;
               position: absolute !important;
               width: 5% !important;
               padding: 1% !important;
               right: 20% !important;
               top: 15% !important;
              }
              ha-card {
               background: none  !important;
               padding: 0 !important;
              }
              .icon > ha-icon {
               width:30% !important;
               height:100% !important;
              }
              .state__time{
               font-size:1vw !important;
               margin-top: 0.2vw;
               font-weight: 300 !important;
               opacity: 0.6 !important;
              }
              .states {
               font-size: 80% !important;
               padding: 1vw 0vw 0vw 0vw  !important;
               margin: auto !important;
               width: 70%;
              }
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/weather
            type: custom:mini-graph-card
          - backdrop: false
            entity: weather.chengdu
            name: ' '
            style: |
              :host {
               left: 14%;
               top:  18%;
               width: 22.5%;
               height: 2%;
               overflow: ;
               height: 2%;
               background: none;
               box-shadow: none;
               font-size: 80%
               }
               ha-card {
               background: none;
               box-shadow: none;
               flex-flow: none;
               padding: 100;
               }
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/weather
            type: custom:simple-weather-card
          - entity: sensor.date
            hold_action:
              action: none
            style:
              color: rgba(255, 255, 255, 0.5)
              font-size: 1.5vw
              font-weight: 300
              left: 19%
              letter-spacing: 0.24vw
              text-align: left
              top: 17%
              width: 30%
            tap_action:
              action: none
            type: state-label
          - entity: sensor.time
            hold_action:
              action: none
            style:
              color: rgba(121, 231, 255, 0.7)
              font-size: 430%
              font-weight: 400
              left: 3.5%
              letter-spacing: '-0.05vw'
              max-width: 1px
              top: 11%
            tap_action:
              action: none
            type: state-label
  - theme: Backend-selected
    title: 媒体
    path: media
    icon: mdi:music
    type: panel
    badges: []
    cards:
      - type: picture-elements
        image: /local/UI/纯背景.png
        elements:
          - type: custom:mini-media-player
            entity: media_player.yun_yin_le
            artwork: none
            info: scroll
            name: 音乐库
            background: none
            style:
              left: 61%
              top: 25%
              width: 50%
          - action: none
            entity: person.jenny
            state_image:
              home: /local/UI/1.头像/在家.png
              not_home: /local/UI/1.头像/不在家.png
            style:
              background-color: rgba(255, 255, 255, 0.0)
              border-radius: 55%
              height: 9.8%
              left: 8.9%
              top: 72%
              width: 7%
            tap_action: none
            type: image
          - action: none
            entity: person.jason
            state_image:
              home: /local/UI/1.头像/在家-J.png
              not_home: /local/UI/1.头像/不在家-J.png
            style:
              background-color: rgba(255, 255, 255, 0.0)
              border-radius: 55%
              height: 9.8%
              left: 18.5%
              top: 72%
              width: 7%
            tap_action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/ON/1-家庭总览.png
            style:
              left: 13.9%
              top: 33.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/plan
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/2-所有设备.png
            style:
              left: 13.9%
              top: 42.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/light
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/3-媒体控制.png
            style:
              left: 13.9%
              top: 51.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/media
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/4-扫地机器人 .png
            style:
              left: 13.9%
              top: 60.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/robot
            hold_action:
              action: none
            type: image
          - color_thresholds:
              - color: '#4dd2ff'
                value: 17
              - color: '#01a4db'
                value: 20
              - color: '#fccd68'
                value: 26
              - color: '#ff1a1a'
                value: 30
            entities:
              - sensor.temperature
            icon: mdi:home-thermometer-outline
            update_interval: 600
            show:
              icon: true
              legend: false
              name: false
            style: |
              :host {
               left: 14%;
               top:  88.6%;
               width: 22.4%;
               overflow: hidden;
               height: 15%;
               background: none  !important;
               box-shadow: none !important;
              }
              .header {
               font-size: 100%;
               position: absolute !important;
               width: 5% !important;
               padding: 1% !important;
               right: 20% !important;
               top: 15% !important;
              }
              ha-card {
               background: none  !important;
               padding: 0 !important;
              }
              .icon > ha-icon {
               width:30% !important;
               height:100% !important;
              }
              .state__time{
               font-size:1vw !important;
               margin-top: 0.2vw;
               font-weight: 300 !important;
               opacity: 0.6 !important;
              }
              .states {
               font-size: 80% !important;
               padding: 1vw 0vw 0vw 0vw  !important;
               margin: auto !important;
               width: 70%;
              }
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/weather
            type: custom:mini-graph-card
          - backdrop: false
            entity: weather.chengdu
            name: ' '
            style: |
              :host {
               left: 14%;
               top:  18%;
               width: 22.5%;
               height: 2%;
               overflow: ;
               height: 2%;
               background: none;
               box-shadow: none;
               font-size: 80%
               }
               ha-card {
               background: none;
               box-shadow: none;
               flex-flow: none;
               padding: 100;
               }
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/weather
            type: custom:simple-weather-card
          - entity: sensor.date
            hold_action:
              action: none
            style:
              color: rgba(255, 255, 255, 0.5)
              font-size: 1.5vw
              font-weight: 300
              left: 19%
              letter-spacing: 0.24vw
              text-align: left
              top: 17%
              width: 30%
            tap_action:
              action: none
            type: state-label
          - entity: sensor.time
            hold_action:
              action: none
            style:
              color: rgba(121, 231, 255, 0.7)
              font-size: 430%
              font-weight: 400
              left: 3.5%
              letter-spacing: '-0.05vw'
              max-width: 1px
              top: 11%
            tap_action:
              action: none
            type: state-label
  - theme: Backend-selected
    title: 天气预报
    path: weather
    icon: mdi:weather-cloudy
    type: panel
    badges: []
    cards:
      - type: picture-elements
        image: /local/UI/纯背景.png
        elements:
          - type: custom:weather-card
            entity: weather.chengdu
            houer_forecast: true
            show_forecast: true
            icon: /hacsfiles/lovelace-colorfulclouds-weather-card/icons/animated/
            name: 成都天气
            secondary_info_attribute: humidity
            number_of_forecasts: '6'
            style: |
              :host {
               left: 61.6%;
               top:  105%;
               width: 70%;
               overflow: hidden;
               height: 200%;
               background: none  !important;
               box-shadow: none !important;
              }
          - action: none
            entity: person.jenny
            state_image:
              home: /local/UI/1.头像/在家.png
              not_home: /local/UI/1.头像/不在家.png
            style:
              background-color: rgba(255, 255, 255, 0.0)
              border-radius: 55%
              height: 9.8%
              left: 8.9%
              top: 72%
              width: 7%
            tap_action: none
            type: image
          - action: none
            entity: person.jason
            state_image:
              home: /local/UI/1.头像/在家-J.png
              not_home: /local/UI/1.头像/不在家-J.png
            style:
              background-color: rgba(255, 255, 255, 0.0)
              border-radius: 55%
              height: 9.8%
              left: 18.5%
              top: 72%
              width: 7%
            tap_action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/ON/1-家庭总览.png
            style:
              left: 13.9%
              top: 33.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/plan
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/2-所有设备.png
            style:
              left: 13.9%
              top: 42.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/light
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/3-媒体控制.png
            style:
              left: 13.9%
              top: 51.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/media
            hold_action:
              action: none
            type: image
          - action: none
            image: /local/UI/2.侧边栏/OFF/4-扫地机器人 .png
            style:
              left: 13.9%
              top: 60.2%
              width: 17.6%
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/robot
            hold_action:
              action: none
            type: image
          - color_thresholds:
              - color: '#4dd2ff'
                value: 17
              - color: '#01a4db'
                value: 20
              - color: '#fccd68'
                value: 26
              - color: '#ff1a1a'
                value: 30
            entities:
              - sensor.temperature
            icon: mdi:home-thermometer-outline
            update_interval: 600
            show:
              icon: true
              legend: false
              name: false
            style: |
              :host {
               left: 14%;
               top:  88.6%;
               width: 22.4%;
               overflow: hidden;
               height: 15%;
               background: none  !important;
               box-shadow: none !important;
              }
              .header {
               font-size: 100%;
               position: absolute !important;
               width: 5% !important;
               padding: 1% !important;
               right: 20% !important;
               top: 15% !important;
              }
              ha-card {
               background: none  !important;
               padding: 0 !important;
              }
              .icon > ha-icon {
               width:30% !important;
               height:100% !important;
              }
              .state__time{
               font-size:1vw !important;
               margin-top: 0.2vw;
               font-weight: 300 !important;
               opacity: 0.6 !important;
              }
              .states {
               font-size: 80% !important;
               padding: 1vw 0vw 0vw 0vw  !important;
               margin: auto !important;
               width: 70%;
              }
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/weather
            type: custom:mini-graph-card
          - backdrop: false
            entity: weather.chengdu
            name: ' '
            style: |
              :host {
               left: 14%;
               top:  18%;
               width: 22.5%;
               height: 2%;
               overflow: ;
               height: 2%;
               background: none;
               box-shadow: none;
               font-size: 80%
               }
               ha-card {
               background: none;
               box-shadow: none;
               flex-flow: none;
               padding: 100;
               }
            tap_action:
              action: navigate
              navigation_path: /lovelace-jason/weather
            type: custom:simple-weather-card
          - entity: sensor.date
            hold_action:
              action: none
            style:
              color: rgba(255, 255, 255, 0.5)
              font-size: 1.5vw
              font-weight: 300
              left: 19%
              letter-spacing: 0.24vw
              text-align: left
              top: 17%
              width: 30%
            tap_action:
              action: none
            type: state-label
          - entity: sensor.time
            hold_action:
              action: none
            style:
              color: rgba(121, 231, 255, 0.7)
              font-size: 430%
              font-weight: 400
              left: 3.5%
              letter-spacing: '-0.05vw'
              max-width: 1px
              top: 11%
            tap_action:
              action: none
            type: state-label
