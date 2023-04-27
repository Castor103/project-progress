# STB 진행상황


## 순서.

### 1. 진척도 뱃지(Badge) 관련 설명
  - ### 1.1. 각 진척도 뱃지 의미 예시
  - ### 1.2. 진척 정도에 따른 뱃지 순서 예시

### 2. 진행상황 STB
  - ### 2.1. Satellite Data Simulator (SDS)
  - ### 2.2. 그 외 Application List

<br/>


## 1. 진척도 뱃지(Badge) 관련 설명

이 후 진행정도를 나타내는 진척도 Badge 에 대한 간략한 설명.

  - ## 1.1. 각 진척도 뱃지 의미 예시

    * ![](https://img.shields.io/badge/-Wait-yellow)
      - (대기 상태)
      - 기능 개발 미진행 상태.
      - 담당자와 구현에 대한 논의가 필요한 상황.

    <br/>
    
    * ![](https://progress-bar.dev/10/?title=Progress)
    * ![](https://progress-bar.dev/90/?title=Progress)
      - (개발 진행 중인 상태)

    <br/>    
        
    * ![](https://progress-bar.dev/100/?title=Test&color=831083)
      - (Test)  
      - 개발이 요구되는 기능을 구현한 상태.
      - FSW와 STB를 연동하여 지속적인 테스트를 통한 검증이 필요한 상태.
      - 요청되는 개선사항이 있는 경우나 누락된 기능 추가하며 테스트하는 상태.
    
    <br/>    

    * ![](https://img.shields.io/badge/-Done-green) <br/>
      - (Done)
      - 기능 개발 완료.
      - 테스트를 통해 기능 동작을 확인하고 필요한 대부분의 기능이 확인된 상태

<br/>

  - ## 1.2. 진척 정도에 따른 뱃지 순서 예시
 
     * ![](https://img.shields.io/badge/-Wait-yellow) ->  ![](https://progress-bar.dev/10/?title=Progress) ->  ![](https://progress-bar.dev/50/?title=Progress) ->  ![](https://progress-bar.dev/100/?title=Test&color=831083) -> ![](https://img.shields.io/badge/-Done-green)


<br/>


## 2. 진행상황 STB

"STB"는 궤도 동역학을 모사해주는 "Orbit Dynamic Simulator"와 위성의 버스 장비 및 장치들의 로직을 모사해주는 "Satellite Data Simulator"로 이루어지며, 그 외 궤도와 자세 정보를 바탕으로 보여주는 위성의 상태를 가시적으로 보여주는 어플리케이션 까지 칭한다.
    
그 중 "Satellite Data Simulator"는 실제 FSW와 연결하여 운영시 사용하게 되는 명령과 텔레메트리 요청에 따른 응답과 상태 모사를 하게 된다.
   
  - ## 2.1. Satellite Data Simulator (SDS)

    + Satellite Data Model / Core 는 Orbit Dynamic Simulator의 다음 시뮬레이션 스텝에 대한 신호 트리거와 궤도 정보 데이터를 교환하는 역할과 각 버스 로직간의 전류 및 On/Off 정보등의 데이터를 관리함.
    + Subsystem Data Simulation Module / Logic Module 실제 FSW의 명령이나 응답요청시 해당 장비 혹은 장치에 맞에 응답 및 상태 변경을 모사해주는 역할을 담당.

    * ## 2.1.1 Satellite Data Model / Core

       + Logic Module 및 궤도 동역학 시뮬레이션과 연동 하기 위해 필요한 기능은 완료.
       
       + 지속적으로 *전류 연동 및 온도 연동 기능은 지속적인 디버깅 필요.*
       
       + 그 외 성능 개선이 필요한 사항 있으면 반영 중.

    * ## 2.1.2. Subsystem Data Simulation Module / Logic Module
    
    <table style="border: 2px; font-size: 16.5px;">
        <tr>
            <td width="80"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/AOCS-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="100"> <img src=https://img.shields.io/badge/XACT50-gray> <br/>
            <img src=https://img.shields.io/badge/Test-purple> <br/>
            </td>
        </tr><tr>
            <td>각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> 필요한 기능 있으면 지속적으로 추가 중. </td>
         </tr><tr>
            <td> 42 Simulator 와 연동 기능 </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td> </td>
    </table>

    <table style="border: 2px;">
        <tr>
            <td width="80"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/EPS-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/BPX-gray> <br/>
            <img src=https://img.shields.io/badge/Test-purple> </td>
        </tr><tr>
            <td>각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
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
            <td rowspan="3"> <img src=https://img.shields.io/badge/ACU-gray> <br/>
            <img src=https://img.shields.io/badge/Test-purple> </td>
        </tr><tr>
            <td>각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> </td>
        </tr><tr>
            <td> 유효 태양 전지 패널 면적을 통한 전력 생산값 가산 기능 </td>
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> (자체확인) 자체테스트를 통한 확인 튜닝 필요 </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/PDU-gray> <br/>
            <img src=https://img.shields.io/badge/-Test-purple> </td>
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
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> FSW와 연결 테스트하면서 지속 테스트 중 </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/Dock-gray> <br/>
            <img src=https://img.shields.io/badge/Test-purple> </td>
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
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> FSW와 연결 테스트하면서 지속 테스트 중 </td>
        </tr>
    </table>

    <table style="border: 2px;">
        <tr>
            <td width="80"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/IFB-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/IFB_BSS-gray> <br/><img src=https://img.shields.io/badge/Test-purple> </td>
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
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> FSW와 연결 테스트하면서 수치 조정 중</td>
        </tr>
        </tr><tr>
            <td rowspan="5"> <img src=https://img.shields.io/badge/IFB_OBS1-gray> <br/><img src=https://img.shields.io/badge/Test-purple> </td>
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
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
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
            <td width="80"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/SP-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="4"> <img src=https://img.shields.io/badge/SP-gray> <br/>
            <img src=https://img.shields.io/badge/-Done-green> </td>
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
            <td width="80"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100"> <img src=https://img.shields.io/badge/CS-1f0000?style=for-the-badge> </td>
        </tr><tr>
            <td rowspan="2"> <img src=https://img.shields.io/badge/AX2150-gray> <br/> <img src=https://img.shields.io/badge/-Done-green> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td rowspan="3"> <img src=https://img.shields.io/badge/EWC27-gray> <img src=https://progress-bar.dev/90/?title=Progress> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://img.shields.io/badge/-Done-green> </td>
            <td/>
        </tr><tr>
            <td> PDHS->EWC27 TF 데이터 교환시 Tx 전류 반영 </td>
            <td> <img src=https://progress-bar.dev/80/?title=Progress> </td>
            <td> 간소화 된 기능으로 구현, Flow에 지장 없는지 확인 필요 </td>
        </tr>
    </table>

    <table style="border: 2px;">
        <tr>
            <td width="80"> Subsystem </td>
            <td width="150"> Component </td>
            <td width="320"> Items </td>
            <td width="130"> Progress </td>
            <td> Memo </td>
        </tr><tr>
            <td rowspan="100">
            <img src=https://img.shields.io/badge/PAYLOAD-1f0000?style=for-the-badge>
            </td>
        </tr><tr>
            <td rowspan="11"> <img src=https://img.shields.io/badge/PDHS-gray> <img src=https://progress-bar.dev/84/?title=Progress> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> FSW와 지속적인 테스트 필요 </td>
        </tr>
            <td> MS200 미션 데이터 수신 기능</td>
            <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> Polcube 미션 데이터와 중복되는 부분이 있지만 특성에 따른 부분 확인 필요 </td>
        </tr>
        </tr><tr>
            <td> Polcube 미션 데이터 수신 기능 </td>
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> 해당 당담자와 테스트 필요 </td>
        </tr><tr>
            <td> OBC 미션 데이터 수신 기능 </td>
            <td> <img src=https://progress-bar.dev/50/?title=Progress> </td>
            <td> 
            1. 구현 논의중. <br/> 
            2. virtual comport 기능 확인중 <br/> 
            3. vcomport rx 적용
            4. 파싱 포멧 ?
            </td>
        </tr>
        </tr><tr>
            <td> 미션 데이터 수신시 세션별 관리 기능 </td>
            <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
            <td> FSW와 지속적인 테스트 필요 </td>
        </tr>
        </tr><tr>
            <td> 미션 데이터 수신시 CRC Error 생성 기능 </td>
             <td> <img src=https://progress-bar.dev/100/?title=Test&color=831083> </td>
             <td> 1FSW와 지속적인 테스트 필요 </td>
        </tr>
        </tr><tr>
            <td> AOS TF 전송시 TF List 관리 기능 </td>
             <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> 1. 간소화 된 기능으로 구현 <br/> 
            2. Flow에 지장 없는지 확인 및 테스트 필요 </td>
        </tr>
        </tr><tr>
            <td> AOS TF 송신 데이터 EWC27 로 전달 기능 기능 </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> 1. 간소화 된 기능으로 구현 <br/> 
            2. Flow에 지장 없는지 확인 및 테스트 필요 </td>
        </tr>
        </tr><tr>
            <td> 미션 데이터 재 수신 기능 </td>
            <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> </td>
        </tr>
        </tr><tr>
            <td> AOS TF 재 송신 기능 </td>
            <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> </td>
        </tr>
        </tr><tr>
            <td rowspan="5"> <img src=https://img.shields.io/badge/MS200-gray> <img src=https://progress-bar.dev/82/?title=Progress> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 지속적인 테스트 필요 </td>
        </tr><tr>
            <td> 세션 기본 관리 (Open/Active/Close) 기능 </td>
            <td> <img src=https://progress-bar.dev/80/?title=Progress> </td>
            <td> Polcube->PDHS 미션데이터 기반으로 작업 중. </td>
        </tr><tr>
            <td> Snapshot/Linescan 시 생성 데이터 용량 계산 및 파라미터 검증 기능  </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> Polcube->PDHS 미션데이터 기반으로 작업 중. </td>
        </tr><tr>
            <td> MS200->PDHS 미션 데이터 교환시 해당 기능 </td>
            <td> <img src=https://progress-bar.dev/70/?title=Progress> </td>
            <td> Polcube->PDHS 미션데이터 기반으로 작업 중. </td>
        </tr>
        </tr><tr>
            <td rowspan="6"> <img src=https://img.shields.io/badge/Polcube-gray> <img src=https://progress-bar.dev/90/?title=Progress> </td>
        </tr><tr>
            <td> 각 TC/TM에 따른 반환 포멧 모사 기능 (더미 데이터으로 전달) </td>
            <td> <img src=https://progress-bar.dev/90/?title=Progress> </td>
            <td> FSW와 지속적인 테스트 필요 </td>
        </tr>
        </tr><tr>
            <td> Polcube 센서 동작에 따른 센서 온도 활성화 시간 지연 반영 </td>
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

* STB 전체적으로 리펙토링 해야할 것들
        - [ ] 기존 enum 형태를 enum class 로 모두 교체

<br/>


  - ## 2.2. 그 외 Application List

    + 그 외의 프로그램들은 현재 필요한 수준에 맞게 지속적인 기능 업데이트 중.

    * ## 2.2.1. Orbit Dynamic Simulator 
        + Space Dynamic Simulator

    * ## 2.2.2. libcsp
        + Library for CubeSat Protocol.

    * ## 2.2.3. cesium
        + Satellite Orbit and Attitude Viewer.

<br/>
