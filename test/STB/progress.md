# STB 진행상황

## *진척도 Badge에 따른 상태 의미*

* ![](https://img.shields.io/badge/-Done-green) <br/>
    - (Done)
    - 기능 개발 완료.
    - FSW와 연동 하여 기능 확인 완료.

    <br/>

* ![](https://progress-bar.dev/90/?title=Progress) <br/>
    - (진행 90% ~ 99%)
    - 기능 개발 완료.
    - "FSW와 연동 테스트" 혹은 "FSW와 연동 없이 zmq 소켓을 통한 테스트"와 함께 점검 중.
    - 지속적인 테스트를 하면서 점검이 필요 .

    <br/>


* ![](https://img.shields.io/badge/-Wait-yellow) <br/>
    - (대기 상태)
    - 기능 개발 미진행 상태.
    - 담당자와 구현에 대한 논의가 필요한 상황.

    <br/>

* Memo 내용 관련
    - *"(자체 확인)"* <br/>
        - FSW 연동 없이 STB <-> Zmq 소켓 통신을 통한 테스트를 통한 기능 확인 완료. <br/>

<br/>

## 1. Satellite Data Simulator (SDS)
Satellite Data Simlation Core and Subsystem Data Simulator.
STB의 핵심! 42Sim 제외..
버스의 각 로직 모듈들을 모사해주는 subsystem data simulator와 이들을 연결해주는 satellite data Simlation core로 이루어짐.

 - ## 1.1. Satellite Data Model / Core

    * "Logic Module" 및 "궤도 동역학 시뮬레이션"과 연동 하기 위해 필요한 기능은 완료.
    * 지속적으로 *전류 연동 및 온도 연동 기능은 지속적인 디버깅 필요.*
    * 그 외 성능 개선이 필요한 사항 있으면 반영 중.

   <br/>

 - ## 1.2. Subsystem Data Simulation Module / Logic Module
  
    <br/>
    <br/>
        
    <table style="border: 2px;">
        <tr>
            <td width="100"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/AOCS-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="100"> <img src=https://img.shields.io/badge/XACT50-gray> <img src=https://img.shields.io/badge/Progress-skyblue> </td>
        </tr><tr>
            <td>각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> 필요한 기능 있으면 지속적으로 추가 중. </td>
         </tr><tr>
            <td> 42 Simulator 와 연동 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td> </td>
    </table>

    <table style="border: 2px;">
        <tr>
            <td width="100"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/EPS-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/BPX-gray> <img src=https://img.shields.io/badge/Progress-skyblue> </td>
        </tr><tr>
            <td>각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/87/?title=Progress> </td>
            <td> FSW와 연결 테스트하면서 실제 장비에 맞게 수정 중. </td>
        </tr><tr>
            <td> BPX_Config 설정 및 해당 설정 반환 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td> 전류 소모에 따른 배터리 전압 변화 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr>
        </tr><tr>
            <td rowspan="3"> <img src=https://img.shields.io/badge/ACU-gray> <img src=https://img.shields.io/badge/Progress-skyblue> </td>
        </tr><tr>
            <td>각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/95/?title=Progress> </td>
            <td> (자체확인) zmq 소켓 통신을 통한 자체 테스트 </td>
        </tr><tr>
            <td> 유효 태양 전지 패널 면적을 통한 전력 생산값 가산 기능 </td>
            <td> <img src=https://progress-bar.dev/95/?title=Progress> </td>
            <td> (자체확인) 자체테스트를 통한 확인 튜닝 필요 </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/PDU-gray> <img src=https://img.shields.io/badge/Progress-skyblue> </td>
        </tr><tr>
            <td>각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td> PDU 스위치 동작에 따른 컴포넌트 On/Off 연동 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td> PDU 스위치 동작에 따른 컴포넌트 On/Off 에 따른 전류 연동 기능 </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress>  </td>
            <td> FSW와 연결 테스트하면서 지속 테스트 중 </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/Dock-gray> <img src=https://img.shields.io/badge/Progress-skyblue> </td>
        </tr><tr>
            <td>각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td> Dock 스위치 동작에 따른 컴포넌트 On/Off 연동 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td> Dock 스위치 동작에 따른 컴포넌트 On/Off 에 따른 전류 연동 기능 </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 연결 테스트하면서 지속 테스트 중 </td>
        </tr>
    </table>

    <table style="border: 2px;">
        <tr>
            <td width="100"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/IFB-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/IFB_BSS-gray> <img src=https://img.shields.io/badge/Progress-skyblue> </td>
        </tr><tr>
            <td> GPIO Set/Get 요청에 대한 처리 및 응답 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td> 써미스터 온도 Read 응답 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr>
        </tr><tr>
            <td> 히터 동작 기능 및 그에 따른 전류 증가 반영 </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 연결 테스트하면서 수치 조정 중</td>
        </tr>
        </tr><tr>
            <td rowspan="5"> <img src=https://img.shields.io/badge/IFB_OBS1-gray> <img src=https://img.shields.io/badge/Progress-skyblue> </td>
        </tr><tr>
            <td> GPIO Set/Get 요청에 대한 처리 및 응답 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green></td>
            <td/>
        </tr><tr>
            <td> 써미스터 온도 Read 응답 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr>
        </tr><tr>
            <td> 히터 동작 기능 및 그에 따른 전류 증가 반영 </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 연결 테스트하면서 수치 조정 중</td>
        </tr>
          </tr><tr>
            <td> 안테나 전개 동작 상태 반영 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr>
    </table>

    <table style="border: 2px;">
        <tr>
            <td width="100"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/SP-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/SP-gray> <img src=https://img.shields.io/badge/-Done-green> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://img.shields.io/badge/-Done-green></td>
            <td/>
        </tr><tr>
            <td> 전개 알고리즘 반영 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green></td>
            <td/>
        </tr><tr>
            <td> 전개 GPIO 상태 반영 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green></td>
            <td/>
        </tr>
    </table>

    <table style="border: 2px;">
        <tr>
            <td width="100"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100"> <img src=https://img.shields.io/badge/CS-1f0000?style=for-the-badge> </td>
        </tr><tr>
            <td rowspan="2"> <img src=https://img.shields.io/badge/AX2150-gray> 
            <img src=https://img.shields.io/badge/-Close-green> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td rowspan="3"> <img src=https://img.shields.io/badge/EWC27-gray> <img src=https://img.shields.io/badge/-Done-green> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td> PDHS->EWC27 TF 데이터 교환시 Tx 전류 반영 </td>
            <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> 간소화 된 기능으로 구현, Flow에 지장 없는지 확인 필요 </td>
        </tr>
    </table>

    <table style="border: 2px;">
        <tr>
            <td width="100"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/PAYLOAD-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="11"> <img src=https://img.shields.io/badge/PDHS-gray> <img src=https://img.shields.io/badge/-Progress-skyblue> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 지속적인 테스트 필요 </td>
        </tr>
            <td> MS200 미션 데이터 수신 기능</td>
            <td> <img src=https://progress-bar.dev/10/?title=Progress> </td>
            <td> Polcube 미션 데이터와 중복되는 부분이 있지만 특성에 따른 부분 확인 필요 </td>
        </tr>
        </tr><tr>
            <td> Polcube 미션 데이터 수신 기능 </td>
            <td> <img src=https://progress-bar.dev/80/?title=Progress> </td>
            <td> 해당 당담자와 테스트 필요 </td>
        </tr><tr>
            <td> OBS 미션 데이터 수신 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Wait-yellow> </td>
            <td> 포멧 및 구현 방향에 대한 논의 필요 </td>
        </tr>
        </tr><tr>
            <td> 미션 데이터 수신시 세션별 관리 기능 </td>
            <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> 간소화 된 기능으로 구현, Flow에 지장 없는지 확인 필요 </td>
        </tr>
        </tr><tr>
            <td> 미션 데이터 수신시 CRC Error 생성 기능 </td>
             <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> 간소화 된 기능으로 구현, Flow에 지장 없는지 확인 필요 </td>
        </tr>
        </tr><tr>
            <td> AOS TF 전송시 TF List 관리 기능 </td>
             <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> 간소화 된 기능으로 구현, Flow에 지장 없는지 확인 필요 </td>
        </tr>
        </tr><tr>
            <td> AOS TF 송신 데이터 EWC27 로 전달 기능 기능 </td>
            <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> 간소화 된 기능으로 구현 Flow에 지장 없는지 확인 필요 </td>
        </tr>
        </tr><tr>
            <td> 미션 데이터 재 수신 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Wait-yellow> </td>
            <td> 논의 필요 </td>
        </tr>
        </tr><tr>
            <td> AOS TF 재 송신 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Wait-yellow> </td>
            <td> 논의 필요 </td>
        </tr>
        </tr><tr>
            <td rowspan="3"> <img src=https://img.shields.io/badge/MS200-gray> <img src=https://img.shields.io/badge/-Progress-skyblue> </td>
        </tr><tr>
           <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 지속적인 테스트 필요 </td>
        </tr>
            <td> MS200->PDHS 미션 데이터 교환시 해당 기능 </td>
            <td> <img src=https://progress-bar.dev/10/?title=Progress> </td>
            <td> Polcube->PDHS 미션데이터 기반으로 작업 중. </td>
        </tr>
        </tr><tr>
            <td rowspan="6"> <img src=https://img.shields.io/badge/Polcube-gray> <img src=https://img.shields.io/badge/-Progress-skyblue> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 지속적인 테스트 필요 </td>
        </tr>
        </tr><tr>
            <td> Polcube 센서 동작에 따른 센서 온도 활성화 시간 반영 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr>
        </tr><tr>
            <td> 촬영 및 데이터 전송시 Page 에 따른 데이터 고려 </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 지속적인 테스트 필요 </td>
        </tr>
        </tr><tr>
            <td> POLCUBE->PDHS 미션 데이터 정보 교환 기능 </td>
             <td> <img src=https://progress-bar.dev/80/?title=Progress> </td>
            <td> 간소화 된 기능으로 구현, Flow에 지장 없는지 확인 필요 </td>
        </tr>
    </table>


## 2. 그 외 Application List

그 외의 프로그램들은 현재 필요한 수준에 맞게 지속적인 기능 업데이트 중.
<br/>

 - ## 2. 1. 42 Simulator (42Sim)
Space Dynamic Simulator, Orbit Dynamic Simulator.
<br/>

 - ## 2. 2. libcsp
Library for CubeSat Protocol.
<br/>

 - ## 2. 3. cesium
Satellite Orbit and Attitude Viewer.
<br/>
