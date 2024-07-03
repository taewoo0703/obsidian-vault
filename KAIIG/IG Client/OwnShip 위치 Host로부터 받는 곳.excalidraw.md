---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
MovingModelControl 프로토콜에서 entity 번호 0번으로 해서 Host에서 보내줌. 그러면 이 함수 호출됨 ^l8uR3t9V

CameraControl안의 _position과 _heading, _pitch, _roll을 바꿔줌 ^0ZjZVYMQ

IG-Server에서 온 패킷 처리 ^PxfRlUQB

(그 중에 하나) ^bOsjgct0

_cameraPosition : ENU -> EUS 변환
                  (OSG 기본좌표계 -> OpenGL 기본좌표계) ^sq2LWTc7

_cameraPostion : ECEF -> ENU 변환 ^A6ZmTuzh

_cameraViewport : OpenGL 좌표계 -> 뷰포트 적용한 걸로 변환 ^s3rRk8FK

_matrix : EUS 좌표계 ^hdsLq5pZ

_matrix : ENU 좌표계 ^Tpp1wEnQ

_matrix : Yaw,Pitch,Roll 까지 적용 ^0M7Z1A51

_matrix : Viewport Offset 및 Viewport 방향까지 적용 ^PLxCilI9

_cameraMatrix에 넣어줌 ^bXgoWOkf

_attitude 멤버 업데이트(_heading, _pitch, _roll으로) ^YWPVbEXV

_matrix의 Inverse를 Viewer의 ViewMatrix로 지정해줌.
(osgViewer인데 OpenGL좌표계를 ViewMatrix로 쓴다는 점 유의!) ^qhuxe991

CameraContorl:: UpdateCamera() ^aQei0f5J

KAIIGMain:: RunIG() ^m1ZBVwtJ

CameraControl에서 _position, _heading, _pitch, _roll은 Host로부터 받아온 값으로 ProcessUIPacket 단계에서 업데이트 됨.
나중에 UpdateCamera단계에서 _attitude의 값을 _heading, _pitch, _roll의 값으로 맞춰줌  ^DsVNNybe

EntityID가 0일 때(Ownship) ^yxWnwoRf

EntityID가 0이 아닐 때(MovingModel) ^hcnk8XyP

이걸 업데이트하면 매프레임 호출되는 
KAIIGMain::UpdateControls() 에서 _playerControl->UpdatePlayersList(_modelLoader);
이 호출되면서 GeoTransform의 멤버인 GeoPoint _position을 동일하게 업데이트 해준다.
!!!!!! 단위 조심 !!!!! 
GEODETIC_POSITION의 경우 --- longitude : deg, latitude : deg, altitude : feet
Geopoint의 경우 --- x : long(deg), y : lat(deg), z : alt(meter)이다.
 ^M19KAWGy


# Embedded files
1b9f77ace28a87c0ec314f7bb442b1aaa67c4871: [[KAIIGMain_SetViewPort.png]]
bf1db972b9a8b2dd4e1b681e04a3fea0ed34d542: [[CameraControl 선언일부.png]]
c48c092e00806d69a5e8603f002488248a8aa1e8: [[KAIIGMain_RunIG.png]]
356494a21517192f47a586230ef3a27b19eae3b1: [[CameraControl_UpdateCamera.png]]
29044d251c8def1395c8679c89fad34c35a4a307: [[Pasted Image 20240618124644_493.png]]
1127bae2ad7d92efbb3c7df92e6834b07cc4aa03: [[Pasted Image 20240618124815_526.png]]
5f6f9d4ed0f16f2d3edca2b45bf6cf4ae304d003: [[Pasted Image 20240618125239_656.png]]
e3347f168c2325cefe556bff82e86d245e6c29e5: [[Pasted Image 20240618125355_690.png]]
9ef07e5089630ce0ef11e4b1c69fb83b1777d629: [[Pasted Image 20240618125455_723.png]]
b9304b8c2409424a5e2e87fb8963acf895acaed8: [[Pasted Image 20240618153755_262.png]]
84c2ef90d0751b45bc17d786bb159096b913b5fb: [[Pasted Image 20240618153857_324.png]]
c84868ea467f170673d930f4fb34b50dd36af4f4: [[Pasted Image 20240618154657_508.png]]

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.0.21",
	"elements": [
		{
			"type": "image",
			"version": 263,
			"versionNonce": 1139342801,
			"isDeleted": false,
			"id": "A9uq1gAR4NKeY9XnJjc5J",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -217.71210987362952,
			"y": -686.2266127501149,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 728,
			"height": 192,
			"seed": 143970328,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "c5baXTRYPcGGXMYHvmM0i",
					"type": "arrow"
				}
			],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "1b9f77ace28a87c0ec314f7bb442b1aaa67c4871",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 297,
			"versionNonce": 160121791,
			"isDeleted": false,
			"id": "l8uR3t9V",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -217.71210987362952,
			"y": -721.2266127501149,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 954.2597045898438,
			"height": 25,
			"seed": 16700264,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "MovingModelControl 프로토콜에서 entity 번호 0번으로 해서 Host에서 보내줌. 그러면 이 함수 호출됨",
			"rawText": "MovingModelControl 프로토콜에서 entity 번호 0번으로 해서 Host에서 보내줌. 그러면 이 함수 호출됨",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "MovingModelControl 프로토콜에서 entity 번호 0번으로 해서 Host에서 보내줌. 그러면 이 함수 호출됨",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "image",
			"version": 187,
			"versionNonce": 445324209,
			"isDeleted": false,
			"id": "Mc3zHeCrESgebDhiPXatv",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 605.2878901263705,
			"y": -684.7266127501149,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 428,
			"height": 133,
			"seed": 1593501464,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "0_U8a2knaiycfVQoQ-XSh",
					"type": "arrow"
				}
			],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "bf1db972b9a8b2dd4e1b681e04a3fea0ed34d542",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "arrow",
			"version": 292,
			"versionNonce": 2081059807,
			"isDeleted": false,
			"id": "0_U8a2knaiycfVQoQ-XSh",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 249.28789012637048,
			"y": -606.2266127501149,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 337,
			"height": 10,
			"seed": 1198925336,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "Mc3zHeCrESgebDhiPXatv",
				"focus": 0.06745280136860757,
				"gap": 19
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					337,
					-10
				]
			]
		},
		{
			"type": "rectangle",
			"version": 231,
			"versionNonce": 1995341201,
			"isDeleted": false,
			"id": "k1NTSIKBpX0FyL_64GXqU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 804.2878901263705,
			"y": -687.2266127501149,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 235,
			"height": 58,
			"seed": 55883288,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 304,
			"versionNonce": 326017023,
			"isDeleted": false,
			"id": "zXEdy2G3zMo9Y5beIXYyJ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 772.2878901263705,
			"y": -606.2266127501149,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 176.00000000000003,
			"height": 57.99999999999999,
			"seed": 245063272,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 293,
			"versionNonce": 407544689,
			"isDeleted": false,
			"id": "0ZjZVYMQ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1057.2878901263705,
			"y": -636.2266127501149,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 624.879638671875,
			"height": 25,
			"seed": 1520814360,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "CameraControl안의 _position과 _heading, _pitch, _roll을 바꿔줌",
			"rawText": "CameraControl안의 _position과 _heading, _pitch, _roll을 바꿔줌",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CameraControl안의 _position과 _heading, _pitch, _roll을 바꿔줌",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "image",
			"version": 53,
			"versionNonce": 1639467039,
			"isDeleted": false,
			"id": "QHQvcQxGZosboW_MLshNg",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1241.9764636990155,
			"y": -621.241574754902,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 368.1855072463768,
			"height": 634.6666666666666,
			"seed": 1444115180,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "c48c092e00806d69a5e8603f002488248a8aa1e8",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "arrow",
			"version": 58,
			"versionNonce": 1793527121,
			"isDeleted": false,
			"id": "GxrMtlDEgVU2SEOVMbjIt",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1009.290759588212,
			"y": -497.84353790683235,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 249.82220785077936,
			"height": 1.6381784121362557,
			"seed": 1613256660,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					249.82220785077936,
					-1.6381784121362557
				]
			]
		},
		{
			"type": "text",
			"version": 111,
			"versionNonce": 1691872319,
			"isDeleted": false,
			"id": "PxfRlUQB",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -729.9813403189801,
			"y": -510.9489652039224,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 266.59991455078125,
			"height": 25,
			"seed": 111932372,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "IG-Server에서 온 패킷 처리",
			"rawText": "IG-Server에서 온 패킷 처리",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "IG-Server에서 온 패킷 처리",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 197,
			"versionNonce": 1713060657,
			"isDeleted": false,
			"id": "bOsjgct0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 5.901238938453708,
			"x": -428.3227960280504,
			"y": -576.3527464484065,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 135.0599822998047,
			"height": 25,
			"seed": 1814140756,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "(그 중에 하나)",
			"rawText": "(그 중에 하나)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "(그 중에 하나)",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "arrow",
			"version": 66,
			"versionNonce": 145624159,
			"isDeleted": false,
			"id": "c5baXTRYPcGGXMYHvmM0i",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -446.6137189069657,
			"y": -501.7643136827047,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 197.67906626086426,
			"height": 97.34108701016828,
			"seed": 1707968724,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "A9uq1gAR4NKeY9XnJjc5J",
				"focus": 0.7393314819523643,
				"gap": 31.22254277247191
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					197.67906626086426,
					-97.34108701016828
				]
			]
		},
		{
			"type": "arrow",
			"version": 209,
			"versionNonce": 709799185,
			"isDeleted": false,
			"id": "707-1FA7H-raTU-axS2pJ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1003.3212185852005,
			"y": -145.70731788110163,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 249.77884154652713,
			"height": 0.7007356245833591,
			"seed": 1118978516,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "sTVBHy_tNeTsitPojVWAE",
				"focus": 0.7995690191731094,
				"gap": 24.201402621568263
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					249.77884154652713,
					0.7007356245833591
				]
			]
		},
		{
			"type": "image",
			"version": 217,
			"versionNonce": 1762338943,
			"isDeleted": false,
			"id": "sTVBHy_tNeTsitPojVWAE",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -729.3409744171049,
			"y": -226.82202192652048,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 652.7976355088496,
			"height": 833.515625,
			"seed": 1842315988,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "707-1FA7H-raTU-axS2pJ",
					"type": "arrow"
				}
			],
			"updated": 1718693429497,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "356494a21517192f47a586230ef3a27b19eae3b1",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 309,
			"versionNonce": 1593369329,
			"isDeleted": false,
			"id": "sq2LWTc7",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -279.67740438775905,
			"y": -106.41362359419365,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 567.85986328125,
			"height": 50,
			"seed": 385343084,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_cameraPosition : ENU -> EUS 변환\n                  (OSG 기본좌표계 -> OpenGL 기본좌표계)",
			"rawText": "_cameraPosition : ENU -> EUS 변환\n                  (OSG 기본좌표계 -> OpenGL 기본좌표계)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_cameraPosition : ENU -> EUS 변환\n                  (OSG 기본좌표계 -> OpenGL 기본좌표계)",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 114,
			"versionNonce": 1404027039,
			"isDeleted": false,
			"id": "A6ZmTuzh",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -451.5329158933405,
			"y": -138.21365918774583,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 361.4197998046875,
			"height": 25,
			"seed": 1985324372,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_cameraPostion : ECEF -> ENU 변환",
			"rawText": "_cameraPostion : ECEF -> ENU 변환",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_cameraPostion : ECEF -> ENU 변환",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 89,
			"versionNonce": 1352752337,
			"isDeleted": false,
			"id": "4Qh4faBeIy2YIizqYQVou",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -704.5800076377792,
			"y": -107.76681659817423,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 412.72386621419093,
			"height": 40.59579011942863,
			"seed": 1250488556,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 70,
			"versionNonce": 172774591,
			"isDeleted": false,
			"id": "bU3L5zvU1POtOaaNPJMcu",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -706.6097971437507,
			"y": -132.80088717182187,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 253.72368824642894,
			"height": 18.26810555374287,
			"seed": 2115797868,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 108,
			"versionNonce": 1323276977,
			"isDeleted": false,
			"id": "JbtjbEooQ3eYbhPB-Wyzn",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -695.239715924011,
			"y": 7.59010733373097,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 530.3184789787042,
			"height": 47.7233009394385,
			"seed": 758377684,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 130,
			"versionNonce": 1149330655,
			"isDeleted": false,
			"id": "s3rRk8FK",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -145.0812129592481,
			"y": 22.604179539397023,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 599.2998046875,
			"height": 25,
			"seed": 2118321876,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_cameraViewport : OpenGL 좌표계 -> 뷰포트 적용한 걸로 변환",
			"rawText": "_cameraViewport : OpenGL 좌표계 -> 뷰포트 적용한 걸로 변환",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_cameraViewport : OpenGL 좌표계 -> 뷰포트 적용한 걸로 변환",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 192,
			"versionNonce": 1247485073,
			"isDeleted": false,
			"id": "GigZgZ03siQrEAHpSLjFL",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -698.4570171109397,
			"y": 138.96323913330886,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 180.16886646799253,
			"height": 15.550289070154065,
			"seed": 496091244,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 164,
			"versionNonce": 1910468863,
			"isDeleted": false,
			"id": "hdsLq5pZ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -505.4189458952335,
			"y": 142.1805403202373,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 212.79991149902344,
			"height": 25,
			"seed": 596602964,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_matrix : EUS 좌표계",
			"rawText": "_matrix : EUS 좌표계",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_matrix : EUS 좌표계",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 65,
			"versionNonce": 852189809,
			"isDeleted": false,
			"id": "Mx39mCMG_Yfry97-AJlll",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -697.9208002464517,
			"y": 103.03670921260795,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 271.325733430965,
			"height": 30.02814441133208,
			"seed": 50365140,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 59,
			"versionNonce": 1004992799,
			"isDeleted": false,
			"id": "Tpp1wEnQ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -410.5085608808445,
			"y": 104.64535980607215,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 213.51991271972656,
			"height": 25,
			"seed": 1640450900,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_matrix : ENU 좌표계",
			"rawText": "_matrix : ENU 좌표계",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_matrix : ENU 좌표계",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 81,
			"versionNonce": 351792209,
			"isDeleted": false,
			"id": "BA5zzZuPovwSrQB8lmPKU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -681.8342943118096,
			"y": 185.0778894792831,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 341.0339258144145,
			"height": 43.969782888021996,
			"seed": 1488974956,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 102,
			"versionNonce": 1208515903,
			"isDeleted": false,
			"id": "0M7Z1A51",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -331.1484649366097,
			"y": 195.2660099045565,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 332.9798278808594,
			"height": 25,
			"seed": 683222764,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_matrix : Yaw,Pitch,Roll 까지 적용",
			"rawText": "_matrix : Yaw,Pitch,Roll 까지 적용",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_matrix : Yaw,Pitch,Roll 까지 적용",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 86,
			"versionNonce": 2025339441,
			"isDeleted": false,
			"id": "RA0jNnKI-Xudej3q2X6WZ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -700.601884568892,
			"y": 374.3624426435729,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 441.3064794736841,
			"height": 28.955710682355914,
			"seed": 1792362580,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 95,
			"versionNonce": 967081311,
			"isDeleted": false,
			"id": "PLxCilI9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -249.1072846699346,
			"y": 377.04352696601325,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 517.2996826171875,
			"height": 25,
			"seed": 386917228,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_matrix : Viewport Offset 및 Viewport 방향까지 적용",
			"rawText": "_matrix : Viewport Offset 및 Viewport 방향까지 적용",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_matrix : Viewport Offset 및 Viewport 방향까지 적용",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 91,
			"versionNonce": 2129906705,
			"isDeleted": false,
			"id": "bXgoWOkf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -552.606029970184,
			"y": 426.9116953634039,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 239.61988830566406,
			"height": 25,
			"seed": 195368300,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_cameraMatrix에 넣어줌",
			"rawText": "_cameraMatrix에 넣어줌",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_cameraMatrix에 넣어줌",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 61,
			"versionNonce": 1946909055,
			"isDeleted": false,
			"id": "ThjLS4GtSgfLd1ZzfMFAK",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -698.9932339754279,
			"y": 452.65010485883147,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 52.5492527198312,
			"height": 24.129758901963328,
			"seed": 1930561748,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 193,
			"versionNonce": 1067590129,
			"isDeleted": false,
			"id": "YWPVbEXV",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -637.3282945592994,
			"y": 454.25875545229576,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 521.65966796875,
			"height": 25,
			"seed": 712971604,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_attitude 멤버 업데이트(_heading, _pitch, _roll으로)",
			"rawText": "_attitude 멤버 업데이트(_heading, _pitch, _roll으로)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_attitude 멤버 업데이트(_heading, _pitch, _roll으로)",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 63,
			"versionNonce": 478015903,
			"isDeleted": false,
			"id": "VH8t7csxlIep9Y8PxOGYK",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -701.6743182978685,
			"y": 408.6803219708096,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 365.1636847163778,
			"height": 17.695156528106395,
			"seed": 650631276,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "KrK3GxK-pGNWw6BXE18Xp",
					"type": "arrow"
				}
			],
			"updated": 1718693429498,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 129,
			"versionNonce": 1741339601,
			"isDeleted": false,
			"id": "KrK3GxK-pGNWw6BXE18Xp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -326.1208981761799,
			"y": 423.76244680122863,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 280.0136052418587,
			"height": 2.2234332530404117,
			"seed": 105363692,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "VH8t7csxlIep9Y8PxOGYK",
				"focus": 0.39427088412705524,
				"gap": 10.389735405310773
			},
			"endBinding": {
				"elementId": "qhuxe991",
				"focus": 0.3874731262882655,
				"gap": 14.015480859068703
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					280.0136052418587,
					2.2234332530404117
				]
			]
		},
		{
			"type": "text",
			"version": 338,
			"versionNonce": 1546413503,
			"isDeleted": false,
			"id": "qhuxe991",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -32.09181207525239,
			"y": 414.06027829288547,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 594.759765625,
			"height": 50,
			"seed": 1735317588,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "KrK3GxK-pGNWw6BXE18Xp",
					"type": "arrow"
				}
			],
			"updated": 1718693429498,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "_matrix의 Inverse를 Viewer의 ViewMatrix로 지정해줌.\n(osgViewer인데 OpenGL좌표계를 ViewMatrix로 쓴다는 점 유의!)",
			"rawText": "_matrix의 Inverse를 Viewer의 ViewMatrix로 지정해줌.\n(osgViewer인데 OpenGL좌표계를 ViewMatrix로 쓴다는 점 유의!)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "_matrix의 Inverse를 Viewer의 ViewMatrix로 지정해줌.\n(osgViewer인데 OpenGL좌표계를 ViewMatrix로 쓴다는 점 유의!)",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "text",
			"version": 89,
			"versionNonce": 1185230491,
			"isDeleted": false,
			"id": "aQei0f5J",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -725.8171655469802,
			"y": -278.7246900301644,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 574.019775390625,
			"height": 45,
			"seed": 2095915860,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718962826982,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "CameraContorl:: UpdateCamera()",
			"rawText": "CameraContorl:: UpdateCamera()",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CameraContorl:: UpdateCamera()",
			"lineHeight": 1.25,
			"baseline": 31
		},
		{
			"type": "text",
			"version": 53,
			"versionNonce": 1149164693,
			"isDeleted": false,
			"id": "m1ZBVwtJ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -1239.7399325698807,
			"y": -675.0412809260567,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 361.83587646484375,
			"height": 45,
			"seed": 1925123564,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718962826983,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "KAIIGMain:: RunIG()",
			"rawText": "KAIIGMain:: RunIG()",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "KAIIGMain:: RunIG()",
			"lineHeight": 1.25,
			"baseline": 31
		},
		{
			"type": "text",
			"version": 855,
			"versionNonce": 1826267963,
			"isDeleted": false,
			"id": "DsVNNybe",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 911.1140534161359,
			"y": 208.32476058658335,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 2140.41552734375,
			"height": 90,
			"seed": 1017948652,
			"groupIds": [],
			"frameId": "kNmwiXvJUmMdHD2bXBvnB",
			"roundness": null,
			"boundElements": [],
			"updated": 1718962826988,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "CameraControl에서 _position, _heading, _pitch, _roll은 Host로부터 받아온 값으로 ProcessUIPacket 단계에서 업데이트 됨.\n나중에 UpdateCamera단계에서 _attitude의 값을 _heading, _pitch, _roll의 값으로 맞춰줌 ",
			"rawText": "CameraControl에서 _position, _heading, _pitch, _roll은 Host로부터 받아온 값으로 ProcessUIPacket 단계에서 업데이트 됨.\n나중에 UpdateCamera단계에서 _attitude의 값을 _heading, _pitch, _roll의 값으로 맞춰줌 ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CameraControl에서 _position, _heading, _pitch, _roll은 Host로부터 받아온 값으로 ProcessUIPacket 단계에서 업데이트 됨.\n나중에 UpdateCamera단계에서 _attitude의 값을 _heading, _pitch, _roll의 값으로 맞춰줌 ",
			"lineHeight": 1.25,
			"baseline": 76
		},
		{
			"type": "freedraw",
			"version": 117,
			"versionNonce": 1655935377,
			"isDeleted": false,
			"id": "sLnZ71i0lY-xz0BNZ5rwg",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1021.8415933862548,
			"y": -29.65658625202036,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 84.62137923910541,
			"height": 137.50974126354606,
			"seed": 849215212,
			"groupIds": [],
			"frameId": "kNmwiXvJUmMdHD2bXBvnB",
			"roundness": null,
			"boundElements": [],
			"updated": 1718694334517,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-2.6444181012220724,
					5.288836202444031
				],
				[
					-13.222090506110362,
					26.444181012220383
				],
				[
					-26.444181012220724,
					52.88836202444077
				],
				[
					-39.66627151833063,
					71.39928873299505
				],
				[
					-55.53278012566261,
					92.5546335427714
				],
				[
					-71.39928873299505,
					116.35439645376982
				],
				[
					-84.62137923910541,
					134.8653231623241
				],
				[
					-84.62137923910541,
					137.50974126354606
				],
				[
					-84.62137923910541,
					137.50974126354606
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 198,
			"versionNonce": 1917663089,
			"isDeleted": false,
			"id": "DlfnqAc-l0bgOS2RPXaXt",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1027.2416724159216,
			"y": -32.30100435324243,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 92.55463354277163,
			"height": 129.57648695988007,
			"seed": 668288108,
			"groupIds": [],
			"frameId": "kNmwiXvJUmMdHD2bXBvnB",
			"roundness": null,
			"boundElements": [],
			"updated": 1718694334517,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					2.6444181012220724
				],
				[
					0,
					15.866508607332207
				],
				[
					-2.6444181012220724,
					34.37743531588649
				],
				[
					-2.6444181012220724,
					55.53278012566284
				],
				[
					-2.6444181012220724,
					71.39928873299505
				],
				[
					-2.6444181012220724,
					89.91021544154944
				],
				[
					-2.6444181012220724,
					111.06556025132568
				],
				[
					-2.6444181012220724,
					118.9988145549919
				],
				[
					-2.6444181012220724,
					121.64323265621385
				],
				[
					-2.6444181012220724,
					124.28765075743593
				],
				[
					0,
					113.70997835254775
				],
				[
					10.57767240488829,
					100.4878878464375
				],
				[
					21.15534480977658,
					84.6213792391053
				],
				[
					34.37743531588694,
					66.11045253055102
				],
				[
					47.59952582199685,
					47.599525821996735
				],
				[
					55.532780125663066,
					37.02185341710856
				],
				[
					68.75487063177297,
					23.79976291099831
				],
				[
					76.68812493543919,
					15.866508607332207
				],
				[
					81.97696113788334,
					5.288836202444031
				],
				[
					87.26579734032748,
					0
				],
				[
					87.26579734032748,
					-2.6444181012220724
				],
				[
					89.91021544154955,
					-2.6444181012220724
				],
				[
					89.91021544154955,
					0
				],
				[
					89.91021544154955,
					18.51092670855428
				],
				[
					89.91021544154955,
					34.37743531588649
				],
				[
					84.62137923910541,
					50.24394392321881
				],
				[
					81.97696113788334,
					68.75487063177309
				],
				[
					79.33254303666126,
					87.26579734032737
				],
				[
					79.33254303666126,
					103.13230594765957
				],
				[
					79.33254303666126,
					113.70997835254775
				],
				[
					79.33254303666126,
					121.64323265621385
				],
				[
					79.33254303666126,
					126.932068858658
				],
				[
					79.33254303666126,
					126.932068858658
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 139,
			"versionNonce": 259465553,
			"isDeleted": false,
			"id": "ykq-DuqsFIKeVh7IsHReQ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1159.3513346498003,
			"y": 60.25362918952874,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 74.04370683421712,
			"height": 68.75487063177309,
			"seed": 1411720788,
			"groupIds": [],
			"frameId": "kNmwiXvJUmMdHD2bXBvnB",
			"roundness": null,
			"boundElements": [],
			"updated": 1718694334517,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					10.57767240488829,
					-2.6444181012219588
				],
				[
					37.021853417109014,
					-10.577672404888176
				],
				[
					50.24394392321892,
					-13.222090506110135
				],
				[
					55.532780125663066,
					-13.222090506110135
				],
				[
					63.466034429329284,
					-18.51092670855428
				],
				[
					68.75487063177297,
					-21.155344809776352
				],
				[
					71.39928873299505,
					-26.444181012220383
				],
				[
					71.39928873299505,
					-31.733017214664414
				],
				[
					71.39928873299505,
					-37.02185341710856
				],
				[
					71.39928873299505,
					-42.31068961955259
				],
				[
					66.11045253055136,
					-47.599525821996735
				],
				[
					63.466034429329284,
					-50.24394392321881
				],
				[
					55.532780125663066,
					-52.88836202444077
				],
				[
					50.24394392321892,
					-52.88836202444077
				],
				[
					44.95510772077523,
					-52.88836202444077
				],
				[
					37.021853417109014,
					-52.88836202444077
				],
				[
					29.088599113442797,
					-50.24394392321881
				],
				[
					23.799762910998652,
					-50.24394392321881
				],
				[
					21.15534480977658,
					-47.599525821996735
				],
				[
					18.510926708554507,
					-42.31068961955259
				],
				[
					13.222090506110362,
					-39.66627151833063
				],
				[
					10.57767240488829,
					-34.37743531588649
				],
				[
					5.288836202444145,
					-29.088599113442456
				],
				[
					5.288836202444145,
					-15.866508607332207
				],
				[
					5.288836202444145,
					-7.933254303666104
				],
				[
					5.288836202444145,
					0
				],
				[
					5.288836202444145,
					5.288836202444145
				],
				[
					5.288836202444145,
					7.933254303666104
				],
				[
					7.933254303666217,
					10.577672404888176
				],
				[
					13.222090506110362,
					13.222090506110248
				],
				[
					18.510926708554507,
					15.866508607332321
				],
				[
					23.799762910998652,
					15.866508607332321
				],
				[
					26.444181012220724,
					15.866508607332321
				],
				[
					34.37743531588694,
					15.866508607332321
				],
				[
					39.66627151833109,
					15.866508607332321
				],
				[
					47.599525821997304,
					15.866508607332321
				],
				[
					58.17719822688514,
					15.866508607332321
				],
				[
					66.11045253055136,
					15.866508607332321
				],
				[
					71.39928873299505,
					15.866508607332321
				],
				[
					74.04370683421712,
					13.222090506110248
				],
				[
					74.04370683421712,
					13.222090506110248
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 149,
			"versionNonce": 663277361,
			"isDeleted": false,
			"id": "I2SgnITY3KThZsU9hFkbY",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1296.8610759133471,
			"y": -0.5679871385780189,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 113.70997835254775,
			"height": 81.97696113788322,
			"seed": 440922836,
			"groupIds": [],
			"frameId": "kNmwiXvJUmMdHD2bXBvnB",
			"roundness": null,
			"boundElements": [],
			"updated": 1718694334517,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-2.6444181012220724,
					0
				],
				[
					-7.933254303666217,
					2.6444181012219588
				],
				[
					-13.222090506109907,
					7.933254303666104
				],
				[
					-18.510926708554052,
					13.222090506110135
				],
				[
					-21.155344809776125,
					23.79976291099831
				],
				[
					-23.799762910998197,
					31.733017214664414
				],
				[
					-26.44418101222027,
					39.66627151833052
				],
				[
					-31.733017214664414,
					50.243943923218694
				],
				[
					-31.733017214664414,
					55.53278012566284
				],
				[
					-34.37743531588649,
					58.17719822688491
				],
				[
					-34.37743531588649,
					63.46603442932894
				],
				[
					-34.37743531588649,
					66.11045253055102
				],
				[
					-34.37743531588649,
					68.75487063177297
				],
				[
					-34.37743531588649,
					71.39928873299505
				],
				[
					-34.37743531588649,
					74.04370683421712
				],
				[
					-34.37743531588649,
					71.39928873299505
				],
				[
					-31.733017214664414,
					66.11045253055102
				],
				[
					-26.44418101222027,
					60.82161632810687
				],
				[
					-18.510926708554052,
					52.88836202444077
				],
				[
					-13.222090506109907,
					44.95510772077466
				],
				[
					-2.6444181012220724,
					34.37743531588649
				],
				[
					5.288836202444145,
					29.088599113442456
				],
				[
					13.222090506109907,
					21.15534480977624
				],
				[
					15.86650860733198,
					18.51092670855428
				],
				[
					18.510926708554052,
					18.51092670855428
				],
				[
					18.510926708554052,
					15.866508607332207
				],
				[
					18.510926708554052,
					23.79976291099831
				],
				[
					18.510926708554052,
					34.37743531588649
				],
				[
					18.510926708554052,
					47.599525821996735
				],
				[
					18.510926708554052,
					55.53278012566284
				],
				[
					18.510926708554052,
					66.11045253055102
				],
				[
					18.510926708554052,
					68.75487063177297
				],
				[
					18.510926708554052,
					66.11045253055102
				],
				[
					23.799762910998197,
					58.17719822688491
				],
				[
					39.66627151833063,
					42.31068961955259
				],
				[
					52.888362024440994,
					29.088599113442456
				],
				[
					63.46603442932883,
					21.15534480977624
				],
				[
					74.04370683421712,
					13.222090506110135
				],
				[
					76.68812493543919,
					7.933254303666104
				],
				[
					76.68812493543919,
					10.577672404888062
				],
				[
					76.68812493543919,
					15.866508607332207
				],
				[
					76.68812493543919,
					26.444181012220383
				],
				[
					76.68812493543919,
					37.02185341710856
				],
				[
					76.68812493543919,
					50.243943923218694
				],
				[
					76.68812493543919,
					60.82161632810687
				],
				[
					76.68812493543919,
					68.75487063177297
				],
				[
					76.68812493543919,
					76.68812493543919
				],
				[
					76.68812493543919,
					79.33254303666115
				],
				[
					76.68812493543919,
					81.97696113788322
				],
				[
					79.33254303666126,
					81.97696113788322
				],
				[
					79.33254303666126,
					81.97696113788322
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 160,
			"versionNonce": 283754769,
			"isDeleted": false,
			"id": "RPjke6BfVSs95YxhWoBps",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1450.2373257842264,
			"y": 20.587357671198106,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 76.68812493543919,
			"height": 58.17719822688491,
			"seed": 1226791404,
			"groupIds": [],
			"frameId": "kNmwiXvJUmMdHD2bXBvnB",
			"roundness": null,
			"boundElements": [],
			"updated": 1718694334517,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-2.6444181012220724,
					0
				],
				[
					-7.933254303666217,
					0
				],
				[
					-10.57767240488829,
					0
				],
				[
					-10.57767240488829,
					2.6444181012220724
				],
				[
					-15.866508607332435,
					7.933254303666104
				],
				[
					-23.799762910998652,
					13.222090506110248
				],
				[
					-26.444181012220724,
					18.51092670855428
				],
				[
					-26.444181012220724,
					21.155344809776352
				],
				[
					-26.444181012220724,
					23.799762910998425
				],
				[
					-26.444181012220724,
					26.444181012220383
				],
				[
					-26.444181012220724,
					29.088599113442456
				],
				[
					-26.444181012220724,
					31.733017214664528
				],
				[
					-23.799762910998652,
					34.3774353158866
				],
				[
					-21.15534480977658,
					37.02185341710856
				],
				[
					-18.510926708554507,
					39.66627151833063
				],
				[
					-10.57767240488829,
					44.95510772077478
				],
				[
					0,
					50.24394392321881
				],
				[
					7.933254303665763,
					50.24394392321881
				],
				[
					15.86650860733198,
					50.24394392321881
				],
				[
					18.510926708554052,
					50.24394392321881
				],
				[
					21.155344809776125,
					50.24394392321881
				],
				[
					26.44418101222027,
					47.599525821996735
				],
				[
					29.088599113442342,
					47.599525821996735
				],
				[
					31.733017214664414,
					44.95510772077478
				],
				[
					37.02185341710856,
					42.310689619552704
				],
				[
					39.66627151833063,
					39.66627151833063
				],
				[
					44.95510772077432,
					37.02185341710856
				],
				[
					47.599525821996394,
					34.3774353158866
				],
				[
					50.24394392321847,
					26.444181012220383
				],
				[
					50.24394392321847,
					23.799762910998425
				],
				[
					50.24394392321847,
					18.51092670855428
				],
				[
					50.24394392321847,
					13.222090506110248
				],
				[
					50.24394392321847,
					10.577672404888176
				],
				[
					50.24394392321847,
					2.6444181012220724
				],
				[
					47.599525821996394,
					0
				],
				[
					44.95510772077432,
					-5.288836202444031
				],
				[
					42.31068961955225,
					-5.288836202444031
				],
				[
					37.02185341710856,
					-7.933254303666104
				],
				[
					31.733017214664414,
					-7.933254303666104
				],
				[
					29.088599113442342,
					-7.933254303666104
				],
				[
					26.44418101222027,
					-7.933254303666104
				],
				[
					21.155344809776125,
					-7.933254303666104
				],
				[
					15.86650860733198,
					-7.933254303666104
				],
				[
					13.222090506109907,
					-7.933254303666104
				],
				[
					7.933254303665763,
					-7.933254303666104
				],
				[
					2.6444181012216177,
					-7.933254303666104
				],
				[
					-7.933254303666217,
					-5.288836202444031
				],
				[
					-10.57767240488829,
					-5.288836202444031
				],
				[
					-10.57767240488829,
					-5.288836202444031
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "frame",
			"version": 235,
			"versionNonce": 1344475601,
			"isDeleted": false,
			"id": "kNmwiXvJUmMdHD2bXBvnB",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"angle": 0,
			"x": 871.1097616165985,
			"y": -85.18936637768343,
			"strokeColor": "#bbb",
			"backgroundColor": "transparent",
			"width": 2841.8593959372815,
			"height": 2417.908634848205,
			"seed": 1014237652,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718694334517,
			"link": null,
			"locked": false,
			"customData": {
				"frameColor": {
					"stroke": "#D4D4D4",
					"fill": "#ADADAD",
					"nameColor": "#7A7A7A"
				}
			},
			"name": null
		},
		{
			"type": "image",
			"version": 193,
			"versionNonce": 676982367,
			"isDeleted": false,
			"id": "Ntci0ajW76NRPVP4Fedn0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -890.5144298002821,
			"y": -1664.5083737573248,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 633.4079531720021,
			"height": 841.7287911041271,
			"seed": 412943857,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "AWHVPu5DjJLQe2ErkWTlf",
					"type": "arrow"
				}
			],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "29044d251c8def1395c8679c89fad34c35a4a307",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "line",
			"version": 45,
			"versionNonce": 357165841,
			"isDeleted": false,
			"id": "B9ueRwWSjLqGTTr8dPRYI",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -582.8004719475316,
			"y": -532.7270348514903,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 17.200873327430713,
			"height": 286.6812221238454,
			"seed": 172388497,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					17.200873327430713,
					-286.6812221238454
				]
			]
		},
		{
			"type": "rectangle",
			"version": 77,
			"versionNonce": 753584767,
			"isDeleted": false,
			"id": "sJyXZYFkiD4fzPZ8nDXMJ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -831.8931324964788,
			"y": -1261.0474366104195,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 415.71956817081093,
			"height": 16.264458848623235,
			"seed": 931358577,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "A78J88r4m-dw7ISvCrthQ",
					"type": "arrow"
				}
			],
			"updated": 1718693429499,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 166,
			"versionNonce": 64774385,
			"isDeleted": false,
			"id": "TmXbZbPTVrsqkfHiZluri",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -810.0987576393235,
			"y": -1160.5330809259274,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 560.1479627465856,
			"height": 16.91503720256812,
			"seed": 649590321,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 157,
			"versionNonce": 1936696703,
			"isDeleted": false,
			"id": "A78J88r4m-dw7ISvCrthQ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -409.65135356216035,
			"y": -1249.6954595356492,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 331.2058852383758,
			"height": 53.79350094449774,
			"seed": 753090975,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718761049666,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "sJyXZYFkiD4fzPZ8nDXMJ",
				"focus": 0.1022772648761231,
				"gap": 6.52221076350753
			},
			"endBinding": {
				"elementId": "a8U_w4pUC9jmEKqpGfAZ1",
				"focus": -0.14473966210831096,
				"gap": 3.547300845725431
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					200.61583295382036,
					2.033054710979136
				],
				[
					224.0644368055656,
					42.69414893056115
				],
				[
					331.2058852383758,
					53.79350094449774
				]
			]
		},
		{
			"type": "arrow",
			"version": 98,
			"versionNonce": 1987878303,
			"isDeleted": false,
			"id": "AWHVPu5DjJLQe2ErkWTlf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -232.48412446008513,
			"y": -1159.3534646189946,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 152.73595592231493,
			"height": 29.96210492167461,
			"seed": 69536287,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718761049666,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Ntci0ajW76NRPVP4Fedn0",
				"focus": 0.26976648585009805,
				"gap": 24.622352168194936
			},
			"endBinding": {
				"elementId": "a8U_w4pUC9jmEKqpGfAZ1",
				"focus": 0.014765472610003194,
				"gap": 4.850001059711076
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					45.594507489504736,
					-5.210800855943489
				],
				[
					56.01610920139149,
					-29.96210492167461
				],
				[
					152.73595592231493,
					-28.67053907230388
				]
			]
		},
		{
			"type": "image",
			"version": 75,
			"versionNonce": 808154815,
			"isDeleted": false,
			"id": "a8U_w4pUC9jmEKqpGfAZ1",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -74.89816747805912,
			"y": -1381.7041509653125,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 1069,
			"height": 408,
			"seed": 1519258463,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "A78J88r4m-dw7ISvCrthQ",
					"type": "arrow"
				},
				{
					"id": "AWHVPu5DjJLQe2ErkWTlf",
					"type": "arrow"
				}
			],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "1127bae2ad7d92efbb3c7df92e6834b07cc4aa03",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 98,
			"versionNonce": 1400608945,
			"isDeleted": false,
			"id": "yxWnwoRf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 323.01079592783185,
			"y": -1338.6886140399515,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 265.51983642578125,
			"height": 25,
			"seed": 1308978143,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "EntityID가 0일 때(Ownship)",
			"rawText": "EntityID가 0일 때(Ownship)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "EntityID가 0일 때(Ownship)",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 152,
			"versionNonce": 1714177759,
			"isDeleted": false,
			"id": "hcnk8XyP",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 286.55247186042834,
			"y": -1074.2491702595212,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 359.0798034667969,
			"height": 25,
			"seed": 966482033,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "EntityID가 0이 아닐 때(MovingModel)",
			"rawText": "EntityID가 0이 아닐 때(MovingModel)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "EntityID가 0이 아닐 때(MovingModel)",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 59,
			"versionNonce": 382163601,
			"isDeleted": false,
			"id": "HigKmJDPivQ8Xtkv2goEf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -10.11410626931172,
			"y": -1333.948574119724,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 327.2288862290526,
			"height": 20.63605588831865,
			"seed": 2091118431,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "G5muuc0N79gzLaQtCRsod",
					"type": "arrow"
				}
			],
			"updated": 1718693429499,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 102,
			"versionNonce": 534647551,
			"isDeleted": false,
			"id": "mdYo9SiPtaXR0ToQHofn6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 22.313981555189002,
			"y": -1093.1945887560069,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 581.7402421849824,
			"height": 17.68804790427339,
			"seed": 149406239,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "ACS_DqVqFB3zbbqMgzPbA",
					"type": "arrow"
				}
			],
			"updated": 1718693429499,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 205,
			"versionNonce": 1660936305,
			"isDeleted": false,
			"id": "G5muuc0N79gzLaQtCRsod",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 25.666918370293047,
			"y": -1300.7386432186292,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 128.11916497996629,
			"height": 557.2662867014793,
			"seed": 597748753,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "HigKmJDPivQ8Xtkv2goEf",
				"focus": 0.7555372567946268,
				"gap": 12.573875012776057
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-18.749146094629282,
					136.4521187998016
				],
				[
					-113.53649579525484,
					331.23491433844936
				],
				[
					-128.11916497996629,
					557.2662867014793
				]
			]
		},
		{
			"type": "arrow",
			"version": 55,
			"versionNonce": 901864223,
			"isDeleted": false,
			"id": "ACS_DqVqFB3zbbqMgzPbA",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 609.8484476228375,
			"y": -1083.7169569927473,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 498.98830025782695,
			"height": 0.9900561513052253,
			"seed": 1277499199,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "mdYo9SiPtaXR0ToQHofn6",
				"focus": 0.1297323474728406,
				"gap": 5.794223882666074
			},
			"endBinding": {
				"elementId": "3Wa1lTqLdNua2x2FHJV86",
				"focus": -0.03492301007463483,
				"gap": 11.26953558654202
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					498.98830025782695,
					-0.9900561513052253
				]
			]
		},
		{
			"type": "image",
			"version": 44,
			"versionNonce": 99396177,
			"isDeleted": false,
			"id": "3Wa1lTqLdNua2x2FHJV86",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1120.1062834672064,
			"y": -1230.147350051884,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 1019,
			"height": 279,
			"seed": 656286065,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "ACS_DqVqFB3zbbqMgzPbA",
					"type": "arrow"
				}
			],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "5f6f9d4ed0f16f2d3edca2b45bf6cf4ae304d003",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "rectangle",
			"version": 75,
			"versionNonce": 474390335,
			"isDeleted": false,
			"id": "398_DEjzI42hIo6tmEoKT",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1280.3193882279309,
			"y": -1167.2769743046138,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 96.0214297877187,
			"height": 22.373925387429605,
			"seed": 1544038399,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false
		},
		{
			"type": "line",
			"version": 38,
			"versionNonce": 677722161,
			"isDeleted": false,
			"id": "080oX0aww3LhH3mgv_vz1",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1323.2027452205043,
			"y": -1167.276974304614,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 13.051456476000567,
			"height": 153.82073703857827,
			"seed": 1020580049,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					13.051456476000567,
					-153.82073703857827
				]
			]
		},
		{
			"type": "image",
			"version": 73,
			"versionNonce": 1708023647,
			"isDeleted": false,
			"id": "EeIJCqMCaIIVze2t3RwxV",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1125.4060045470762,
			"y": -1348.7426491660503,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 531.3907784900125,
			"height": 24.525728238000575,
			"seed": 943964767,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "e3347f168c2325cefe556bff82e86d245e6c29e5",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "image",
			"version": 32,
			"versionNonce": 1817250321,
			"isDeleted": false,
			"id": "W2IUeqt5rSOORZq9NxqjE",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1592.8270254965346,
			"y": -1604.089114442629,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 792,
			"height": 208,
			"seed": 233376831,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "9ef07e5089630ce0ef11e4b1c69fb83b1777d629",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "line",
			"version": 28,
			"versionNonce": 78191487,
			"isDeleted": false,
			"id": "eNDUMjJ3mOOPM92SwUNEQ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1593.5543436519451,
			"y": -1349.9973649686222,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 26.102912952001134,
			"height": 42.883356992573454,
			"seed": 1811769681,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429499,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					26.102912952001134,
					-42.883356992573454
				]
			]
		},
		{
			"type": "arrow",
			"version": 21,
			"versionNonce": 1252499441,
			"isDeleted": false,
			"id": "cek44so00NKY6zT-NYYdm",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1462.1075320007963,
			"y": -1139.3095675703269,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 149.15950258286375,
			"height": 0.9322468911429951,
			"seed": 1228214833,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429500,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "LFlSLVhwv4e742-3fGYnb",
				"focus": 0.1887717393561003,
				"gap": 13.832735221153257
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					149.15950258286375,
					-0.9322468911429951
				]
			]
		},
		{
			"type": "image",
			"version": 49,
			"versionNonce": 1293374367,
			"isDeleted": false,
			"id": "LFlSLVhwv4e742-3fGYnb",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1625.0997698048134,
			"y": -1162.5128268968983,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 431,
			"height": 52,
			"seed": 2132703217,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "cek44so00NKY6zT-NYYdm",
					"type": "arrow"
				}
			],
			"updated": 1718693429500,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "b9304b8c2409424a5e2e87fb8963acf895acaed8",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "rectangle",
			"version": 62,
			"versionNonce": 829454801,
			"isDeleted": false,
			"id": "cxHVUxxVlPx-J1MYVREl1",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1621.5217503862323,
			"y": -1167.2769743046142,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 433.49480438144775,
			"height": 61.52829481543177,
			"seed": 2018215391,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "kD_62VDdaYco6zVpEiQca",
					"type": "arrow"
				}
			],
			"updated": 1718693429500,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 74,
			"versionNonce": 927565759,
			"isDeleted": false,
			"id": "kD_62VDdaYco6zVpEiQca",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2066.4695745719264,
			"y": -1136.1739209970876,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 149.15950258286375,
			"height": 0.9322468911429951,
			"seed": 1869906897,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429500,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "cxHVUxxVlPx-J1MYVREl1",
				"focus": 0.05495714382704684,
				"gap": 11.453019804246196
			},
			"endBinding": {
				"elementId": "4BPKsM8SOzuUt55AkT5fp",
				"focus": 0.24069892468823428,
				"gap": 12.427448162496603
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					149.15950258286375,
					-0.9322468911429951
				]
			]
		},
		{
			"type": "image",
			"version": 40,
			"versionNonce": 1640175537,
			"isDeleted": false,
			"id": "4BPKsM8SOzuUt55AkT5fp",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2228.0565253172867,
			"y": -1182.779869011718,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 496,
			"height": 117,
			"seed": 1461895889,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "kD_62VDdaYco6zVpEiQca",
					"type": "arrow"
				}
			],
			"updated": 1718693429500,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "84c2ef90d0751b45bc17d786bb159096b913b5fb",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "image",
			"version": 153,
			"versionNonce": 1633695711,
			"isDeleted": false,
			"id": "3DXdEmL5Olqb8TPZUEAfj",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2314.274711469007,
			"y": -1053.6170657916475,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 214,
			"height": 28,
			"seed": 1755054079,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693429500,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "c84868ea467f170673d930f4fb34b50dd36af4f4",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "line",
			"version": 135,
			"versionNonce": 231143825,
			"isDeleted": false,
			"id": "6TeGGB2k9FuoI8v3BRnDN",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2332.4617708361884,
			"y": -1101.0390995003263,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 13.280439720794675,
			"height": 45.651511540234196,
			"seed": 1366222865,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1718693429500,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					13.280439720794675,
					45.651511540234196
				]
			]
		},
		{
			"type": "text",
			"version": 608,
			"versionNonce": 545264849,
			"isDeleted": false,
			"id": "M19KAWGy",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2561.5722505075437,
			"y": -1040.5074646249789,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 839.5393676757812,
			"height": 175,
			"seed": 1367999647,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1718693640214,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "이걸 업데이트하면 매프레임 호출되는 \nKAIIGMain::UpdateControls() 에서 _playerControl->UpdatePlayersList(_modelLoader);\n이 호출되면서 GeoTransform의 멤버인 GeoPoint _position을 동일하게 업데이트 해준다.\n!!!!!! 단위 조심 !!!!! \nGEODETIC_POSITION의 경우 --- longitude : deg, latitude : deg, altitude : feet\nGeopoint의 경우 --- x : long(deg), y : lat(deg), z : alt(meter)이다.\n",
			"rawText": "이걸 업데이트하면 매프레임 호출되는 \nKAIIGMain::UpdateControls() 에서 _playerControl->UpdatePlayersList(_modelLoader);\n이 호출되면서 GeoTransform의 멤버인 GeoPoint _position을 동일하게 업데이트 해준다.\n!!!!!! 단위 조심 !!!!! \nGEODETIC_POSITION의 경우 --- longitude : deg, latitude : deg, altitude : feet\nGeopoint의 경우 --- x : long(deg), y : lat(deg), z : alt(meter)이다.\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "이걸 업데이트하면 매프레임 호출되는 \nKAIIGMain::UpdateControls() 에서 _playerControl->UpdatePlayersList(_modelLoader);\n이 호출되면서 GeoTransform의 멤버인 GeoPoint _position을 동일하게 업데이트 해준다.\n!!!!!! 단위 조심 !!!!! \nGEODETIC_POSITION의 경우 --- longitude : deg, latitude : deg, altitude : feet\nGeopoint의 경우 --- x : long(deg), y : lat(deg), z : alt(meter)이다.\n",
			"lineHeight": 1.25,
			"baseline": 168
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#e03131",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 2,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 2731.170319739234,
		"scrollY": 2125.6445119532973,
		"zoom": {
			"value": 0.15000000000000002
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"gridColor": {
			"Bold": "#C9C9C9FF",
			"Regular": "#EDEDEDFF"
		},
		"currentStrokeOptions": null,
		"previousGridSize": null,
		"frameRendering": {
			"enabled": true,
			"clip": true,
			"name": true,
			"outline": true
		}
	},
	"files": {}
}
```
%%