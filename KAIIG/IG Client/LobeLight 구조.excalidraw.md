---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
프로토콜 ApplyData ^XnhL1W6A

통신으로 받은 LobeLightControlData를 LightManager의 멤버 lightValue[i-1]로 넣어줌 ^eSZ4yOBf

KAIIGMain:: LightControlsSet(int) ^naaHkTmc

EnvironmentControl:: LightControlsSet ^B9rCoBuI

enable일 때 ^sZpZmNy1

EnvironmentControl:: LightControlsAdd ^YhvqFiwL

Light 신규생성 ^lGCAwXPQ

LightManager:: AddLight ^VLNBM6jG

LightControl:: addLights ^C4KcuSkY

프로토콜에서 LightEnable 이면 ^bIAAFk76

1. lightManager->AddLight 호출


2. lightManager->Setting 메소드 호출 ^LwYkmOIV

<Light를 Add할 때>
1.  만약 UpdateCallback이 안 들어가 있으면 콜백에 하나 넣어주자
2. Light를 Add하고 각종 pointer들을 연결시켜주자
    * 값 Setting 하는 건 따로 하자 ^0tAZ91sl

이미 존재하는지 확인하고 Add하는 걸로 여기서 고치자! ^0gvhIq4m

<Light를 Set할 때>
1.  Light 관련 값들 세팅 ^xT7Aiedf

KAIIGMain::UpdateControls() ^RhVa82pj

(매 프레임 호출됨) ^7amV0pP8

HAT, CameraPosition, CameraAttitude, OwnshipSpeed, Viewport Offset ^Xbx5Hwwp


# Embedded files
2a429a00586db531c5b6d35436c2d543312c7213: [[LobeLightControl_ApplyData.png]]
149cb44528010605ba70d55d7c7b308e0382c893: [[KAIIGMain_LightControlsSet.png]]
cd61cfe2aa9dc3f9e56536db581ad293d3a43f6f: [[EnvironmentControl_LightControlsSet.png]]
9b4cce8d215ebd8b770514005c9722551a650755: [[EnvironmentControl_LightControlsAdd.png]]
5de54464186647b4442ac4d0625f5c033109f827: [[LightManager_AddLight.png]]
40255d732f4189ff17f14d225ede3f2aa45439e9: [[LightControl_addLights.png]]
e092ad37aea8bbecb9c8e27ca6fdfded7da7da3d: [[Pasted Image 20240226092351_309.png]]
73b296aa34d21e4f661ea8e5123ef46ef6219391: [[Pasted Image 20240226102428_618.png]]

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
			"version": 11,
			"versionNonce": 1215485643,
			"isDeleted": false,
			"id": "F7tlRNCCZ7Q_WfJpgpcWi",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -901,
			"y": -196.7421875,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 898,
			"height": 71,
			"seed": 2134881236,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "2a429a00586db531c5b6d35436c2d543312c7213",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 63,
			"versionNonce": 1306726245,
			"isDeleted": false,
			"id": "XnhL1W6A",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -894.1709866465638,
			"y": -250.1589254751454,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 343.90789794921875,
			"height": 45,
			"seed": 320874988,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "프로토콜 ApplyData",
			"rawText": "프로토콜 ApplyData",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "프로토콜 ApplyData",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "arrow",
			"version": 569,
			"versionNonce": 1092863339,
			"isDeleted": false,
			"id": "eokqn8Q3qBPSFvu9WdFC-",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -13.227904440838756,
			"y": -174.16539985003112,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 73.34930611637708,
			"height": 66.91416390134532,
			"seed": 1902391124,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "eSZ4yOBf",
				"focus": 0.7972824526480822,
				"gap": 3.981771035320662
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
					39.048118183094516,
					-9.693771473858504
				],
				[
					43.5229359496077,
					-64.35598542697903
				],
				[
					73.34930611637708,
					-66.91416390134532
				]
			]
		},
		{
			"type": "text",
			"version": 197,
			"versionNonce": 670423749,
			"isDeleted": false,
			"id": "eSZ4yOBf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 64.10317271085898,
			"y": -251.0247229972033,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 813.2195434570312,
			"height": 25,
			"seed": 655459436,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "eokqn8Q3qBPSFvu9WdFC-",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "통신으로 받은 LobeLightControlData를 LightManager의 멤버 lightValue[i-1]로 넣어줌",
			"rawText": "통신으로 받은 LobeLightControlData를 LightManager의 멤버 lightValue[i-1]로 넣어줌",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "통신으로 받은 LobeLightControlData를 LightManager의 멤버 lightValue[i-1]로 넣어줌",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "image",
			"version": 77,
			"versionNonce": 1593696267,
			"isDeleted": false,
			"id": "sRinc6vKA6fnCR9daXMsM",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -284.58989260730607,
			"y": -32.78475150501356,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 690,
			"height": 88,
			"seed": 515826924,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "FDPtyJxYP8lpvhQd9Miro",
					"type": "arrow"
				},
				{
					"id": "2qgXhEdqAlHJXLuV2d0BI",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "149cb44528010605ba70d55d7c7b308e0382c893",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "arrow",
			"version": 219,
			"versionNonce": 5782053,
			"isDeleted": false,
			"id": "FDPtyJxYP8lpvhQd9Miro",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -442.97987695991327,
			"y": -145.8753500863528,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 145.095278681946,
			"height": 152.9000172284659,
			"seed": 744693716,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "sRinc6vKA6fnCR9daXMsM",
				"focus": -0.5319417804956644,
				"gap": 13.294705670661187
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
					44.52132621298853,
					20.896704612959297
				],
				[
					65.47423297735469,
					140.32827316984628
				],
				[
					145.095278681946,
					152.9000172284659
				]
			]
		},
		{
			"type": "text",
			"version": 63,
			"versionNonce": 2080089771,
			"isDeleted": false,
			"id": "naaHkTmc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -282.4055068071131,
			"y": -78.08141150171838,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 589.427734375,
			"height": 45,
			"seed": 876285036,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "KAIIGMain:: LightControlsSet(int)",
			"rawText": "KAIIGMain:: LightControlsSet(int)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "KAIIGMain:: LightControlsSet(int)",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "image",
			"version": 57,
			"versionNonce": 267890053,
			"isDeleted": false,
			"id": "wEbhoIbdBxYywI8u3jB-2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 589.2419375758973,
			"y": -37.328229437812354,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 633.1897214847812,
			"height": 543.8206016355779,
			"seed": 1153328364,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "2qgXhEdqAlHJXLuV2d0BI",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "cd61cfe2aa9dc3f9e56536db581ad293d3a43f6f",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "arrow",
			"version": 155,
			"versionNonce": 1321703755,
			"isDeleted": false,
			"id": "2qgXhEdqAlHJXLuV2d0BI",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 417.8711128615122,
			"y": 9.403216482765515,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 149.31504569994604,
			"height": 0.8532288325711193,
			"seed": 922540116,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "sRinc6vKA6fnCR9daXMsM",
				"focus": 0.005016209239298431,
				"gap": 12.461005468818257
			},
			"endBinding": {
				"elementId": "wEbhoIbdBxYywI8u3jB-2",
				"focus": 0.8328500585872672,
				"gap": 22.055779014439054
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
					149.31504569994604,
					-0.8532288325711193
				]
			]
		},
		{
			"type": "text",
			"version": 203,
			"versionNonce": 370259173,
			"isDeleted": false,
			"id": "B9rCoBuI",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 585.2084143926078,
			"y": -91.891594798266,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 652.499755859375,
			"height": 45,
			"seed": 1061244396,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "EnvironmentControl:: LightControlsSet",
			"rawText": "EnvironmentControl:: LightControlsSet",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "EnvironmentControl:: LightControlsSet",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "rectangle",
			"version": 49,
			"versionNonce": 1421621227,
			"isDeleted": false,
			"id": "E_08bmSa7xI7aFKLOGgZm",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 632.0821141870972,
			"y": 1.3120940458350105,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 304.96405454044316,
			"height": 16.205819323405194,
			"seed": 339162604,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "Z5S8csc-id6ZXp72fDB5H",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 175,
			"versionNonce": 238276677,
			"isDeleted": false,
			"id": "Z5S8csc-id6ZXp72fDB5H",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 949.5688472956261,
			"y": 6.468491103282133,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 474.58415385939554,
			"height": 0.7304097191466781,
			"seed": 830361324,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "E_08bmSa7xI7aFKLOGgZm",
				"focus": -0.32294255280220674,
				"gap": 12.52267856808578
			},
			"endBinding": {
				"elementId": "laeilfIErOQWeu2CgLvI0",
				"focus": 0.7803313500145537,
				"gap": 25.46323018166197
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
					474.58415385939554,
					-0.7304097191466781
				]
			]
		},
		{
			"type": "text",
			"version": 82,
			"versionNonce": 2078540427,
			"isDeleted": false,
			"id": "sZpZmNy1",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 814.0292674998736,
			"y": -28.465826111613993,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 109.97994995117188,
			"height": 25,
			"seed": 1812045012,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "enable일 때",
			"rawText": "enable일 때",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "enable일 때",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "image",
			"version": 160,
			"versionNonce": 641433509,
			"isDeleted": false,
			"id": "laeilfIErOQWeu2CgLvI0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1449.6162313366838,
			"y": -32.94876000296563,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 803.9104270581354,
			"height": 350.6349999064032,
			"seed": 1238884972,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "Z5S8csc-id6ZXp72fDB5H",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "9b4cce8d215ebd8b770514005c9722551a650755",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 250,
			"versionNonce": 217676075,
			"isDeleted": false,
			"id": "YhvqFiwL",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1446.9550423144174,
			"y": -85.44339866634715,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 655.1637573242188,
			"height": 45,
			"seed": 316085460,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "EnvironmentControl:: LightControlsAdd",
			"rawText": "EnvironmentControl:: LightControlsAdd",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "EnvironmentControl:: LightControlsAdd",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "rectangle",
			"version": 45,
			"versionNonce": 1951810309,
			"isDeleted": false,
			"id": "3FEQpihhkdeFp8RvcdjMi",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1506.4012485490223,
			"y": 7.000829233707648,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 412.54128895498775,
			"height": 15.567595809622176,
			"seed": 1038301932,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 52,
			"versionNonce": 1432820683,
			"isDeleted": false,
			"id": "lGCAwXPQ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1932.8421766197441,
			"y": 4.77688697519018,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 137.55995178222656,
			"height": 25,
			"seed": 528632940,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "HVglDmAuWH1fALjCLA5i-",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Light 신규생성",
			"rawText": "Light 신규생성",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Light 신규생성",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "arrow",
			"version": 265,
			"versionNonce": 1828821605,
			"isDeleted": false,
			"id": "HVglDmAuWH1fALjCLA5i-",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2081.2488235574133,
			"y": 14.287075056757487,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 309.3909654630361,
			"height": 206.67239611990084,
			"seed": 1529634260,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "lGCAwXPQ",
				"focus": 0.269381549356853,
				"gap": 10.846695155442262
			},
			"endBinding": {
				"elementId": "q698enJE3clE_6p4hFxq0",
				"focus": 0.6866096570679726,
				"gap": 5.821516104152579
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
					180.1372135154793,
					-18.74260025016548
				],
				[
					212.41613616854193,
					-191.5910247794692
				],
				[
					309.3909654630361,
					-206.67239611990084
				]
			]
		},
		{
			"type": "image",
			"version": 75,
			"versionNonce": 289892971,
			"isDeleted": false,
			"id": "q698enJE3clE_6p4hFxq0",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2396.461305124602,
			"y": -265.9919951943209,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 900,
			"height": 324,
			"seed": 1320666476,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "HVglDmAuWH1fALjCLA5i-",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "5de54464186647b4442ac4d0625f5c033109f827",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 324,
			"versionNonce": 420152773,
			"isDeleted": false,
			"id": "VLNBM6jG",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2404.715444934158,
			"y": -320.02712578521306,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 416.8438720703125,
			"height": 45,
			"seed": 1689506796,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "LightManager:: AddLight",
			"rawText": "LightManager:: AddLight",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "LightManager:: AddLight",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "rectangle",
			"version": 112,
			"versionNonce": 358933771,
			"isDeleted": false,
			"id": "ddX88jXHN76NMr6oEN-NU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2455.041939884594,
			"y": -125.73751548543214,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 567.5580795980086,
			"height": 67.41111290244544,
			"seed": 1536629332,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 189,
			"versionNonce": 193987877,
			"isDeleted": false,
			"id": "TTUkXNbzButW9EB9rbOlJ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3033.472779628158,
			"y": -93.11923504876495,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 341.40466857044976,
			"height": 2.174552029111112,
			"seed": 689962220,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "M-Z62gRjTlJRTvcg2Q0uA",
				"focus": -0.4097194627259815,
				"gap": 23.404549580212233
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
					341.40466857044976,
					-2.174552029111112
				]
			]
		},
		{
			"type": "image",
			"version": 194,
			"versionNonce": 960105387,
			"isDeleted": false,
			"id": "M-Z62gRjTlJRTvcg2Q0uA",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3398.28199777882,
			"y": -493.8847638628882,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 828.6914378029078,
			"height": 559.9999999999999,
			"seed": 1839403244,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "TTUkXNbzButW9EB9rbOlJ",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "40255d732f4189ff17f14d225ede3f2aa45439e9",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 368,
			"versionNonce": 402528389,
			"isDeleted": false,
			"id": "C4KcuSkY",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 3405.817307008232,
			"y": -548.5184811860971,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 416.33984375,
			"height": 45,
			"seed": 834232020,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "LightControl:: addLights",
			"rawText": "LightControl:: addLights",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "LightControl:: addLights",
			"lineHeight": 1.25,
			"baseline": 32
		},
		{
			"type": "text",
			"version": 432,
			"versionNonce": 15818315,
			"isDeleted": false,
			"id": "bIAAFk76",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 542.4358523816438,
			"y": 527.4348726576535,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 290.07989501953125,
			"height": 25,
			"seed": 1987290860,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "guAM44_6yHTK_ouvEC9ul",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "프로토콜에서 LightEnable 이면",
			"rawText": "프로토콜에서 LightEnable 이면",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "프로토콜에서 LightEnable 이면",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "text",
			"version": 712,
			"versionNonce": 1209188325,
			"isDeleted": false,
			"id": "LwYkmOIV",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 955.5286621479543,
			"y": 528.3338859956476,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 358.8197937011719,
			"height": 100,
			"seed": 1775634540,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "guAM44_6yHTK_ouvEC9ul",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "1. lightManager->AddLight 호출\n\n\n2. lightManager->Setting 메소드 호출",
			"rawText": "1. lightManager->AddLight 호출\n\n\n2. lightManager->Setting 메소드 호출",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "1. lightManager->AddLight 호출\n\n\n2. lightManager->Setting 메소드 호출",
			"lineHeight": 1.25,
			"baseline": 93
		},
		{
			"type": "arrow",
			"version": 734,
			"versionNonce": 124083435,
			"isDeleted": false,
			"id": "guAM44_6yHTK_ouvEC9ul",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 841.4013374856352,
			"y": 542.3552894846496,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 101.72886545065558,
			"height": 9.378936224096151,
			"seed": 108218476,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "bIAAFk76",
				"focus": -0.2685492784099839,
				"gap": 8.885590084460091
			},
			"endBinding": {
				"elementId": "LwYkmOIV",
				"focus": 0.1339901333799489,
				"gap": 12.398459211663521
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
					101.72886545065558,
					9.378936224096151
				]
			]
		},
		{
			"type": "text",
			"version": 683,
			"versionNonce": 299596613,
			"isDeleted": false,
			"id": "0tAZ91sl",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1544.8736159449961,
			"y": 385.3603953317742,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 632.0198974609375,
			"height": 100,
			"seed": 651641428,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "<Light를 Add할 때>\n1.  만약 UpdateCallback이 안 들어가 있으면 콜백에 하나 넣어주자\n2. Light를 Add하고 각종 pointer들을 연결시켜주자\n    * 값 Setting 하는 건 따로 하자",
			"rawText": "<Light를 Add할 때>\n1.  만약 UpdateCallback이 안 들어가 있으면 콜백에 하나 넣어주자\n2. Light를 Add하고 각종 pointer들을 연결시켜주자\n    * 값 Setting 하는 건 따로 하자",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "<Light를 Add할 때>\n1.  만약 UpdateCallback이 안 들어가 있으면 콜백에 하나 넣어주자\n2. Light를 Add하고 각종 pointer들을 연결시켜주자\n    * 값 Setting 하는 건 따로 하자",
			"lineHeight": 1.25,
			"baseline": 93
		},
		{
			"type": "text",
			"version": 229,
			"versionNonce": 673220491,
			"isDeleted": false,
			"id": "0gvhIq4m",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1000.1741119918477,
			"y": 559.737338845738,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 417.4399719238281,
			"height": 20,
			"seed": 826799468,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "이미 존재하는지 확인하고 Add하는 걸로 여기서 고치자!",
			"rawText": "이미 존재하는지 확인하고 Add하는 걸로 여기서 고치자!",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "이미 존재하는지 확인하고 Add하는 걸로 여기서 고치자!",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 900,
			"versionNonce": 1303759525,
			"isDeleted": false,
			"id": "xT7Aiedf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1550.5443367896617,
			"y": 602.4507093964174,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 228.45994567871094,
			"height": 50,
			"seed": 121758444,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "xLd-X9EV79I_1tB7Wu7lU",
					"type": "arrow"
				}
			],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "<Light를 Set할 때>\n1.  Light 관련 값들 세팅",
			"rawText": "<Light를 Set할 때>\n1.  Light 관련 값들 세팅",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "<Light를 Set할 때>\n1.  Light 관련 값들 세팅",
			"lineHeight": 1.25,
			"baseline": 43
		},
		{
			"type": "arrow",
			"version": 42,
			"versionNonce": 1767726635,
			"isDeleted": false,
			"id": "-TJt8dFqxgDdfFjR3rfOo",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1272.2605762714652,
			"y": 537.992467182537,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 247.375730653785,
			"height": 102.91585740939911,
			"seed": 728719980,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
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
					247.375730653785,
					-102.91585740939911
				]
			]
		},
		{
			"type": "arrow",
			"version": 61,
			"versionNonce": 1817128453,
			"isDeleted": false,
			"id": "xLd-X9EV79I_1tB7Wu7lU",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1343.0742396265564,
			"y": 620.1363166744428,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 198.46917797055607,
			"height": 11.351307424691413,
			"seed": 454977108,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "xT7Aiedf",
				"focus": -0.3515337391858644,
				"gap": 9.000919192549418
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
					198.46917797055607,
					11.351307424691413
				]
			]
		},
		{
			"id": "7re9co8cX-IiF0f9cwA3o",
			"type": "image",
			"x": -878.7679719638253,
			"y": 1012.7768216268038,
			"width": 826,
			"height": 37,
			"angle": 0,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 151765931,
			"version": 235,
			"versionNonce": 637952203,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "e092ad37aea8bbecb9c8e27ca6fdfded7da7da3d",
			"scale": [
				1,
				1
			]
		},
		{
			"id": "RhVa82pj",
			"type": "text",
			"x": -871.323527519381,
			"y": 959.2212660712486,
			"width": 506.8438415527344,
			"height": 45,
			"angle": 0,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1849478795,
			"version": 303,
			"versionNonce": 1822762341,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"text": "KAIIGMain::UpdateControls()",
			"rawText": "KAIIGMain::UpdateControls()",
			"fontSize": 36,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 32,
			"containerId": null,
			"originalText": "KAIIGMain::UpdateControls()",
			"lineHeight": 1.25
		},
		{
			"id": "7amV0pP8",
			"type": "text",
			"x": -873.323527519381,
			"y": 926.7212660712486,
			"width": 245.083984375,
			"height": 35,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 297465765,
			"version": 307,
			"versionNonce": 2008420203,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"text": "(매 프레임 호출됨)",
			"rawText": "(매 프레임 호출됨)",
			"fontSize": 28,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 25,
			"containerId": null,
			"originalText": "(매 프레임 호출됨)",
			"lineHeight": 1.25
		},
		{
			"id": "Xbx5Hwwp",
			"type": "text",
			"x": -875.2683823630226,
			"y": 1068.0511664814312,
			"width": 1236.70751953125,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 11143371,
			"version": 416,
			"versionNonce": 1622600203,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"text": "HAT, CameraPosition, CameraAttitude, OwnshipSpeed, Viewport Offset",
			"rawText": "HAT, CameraPosition, CameraAttitude, OwnshipSpeed, Viewport Offset",
			"fontSize": 36,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 32,
			"containerId": null,
			"originalText": "HAT, CameraPosition, CameraAttitude, OwnshipSpeed, Viewport Offset",
			"lineHeight": 1.25
		},
		{
			"id": "Z-Cox0eI_-jKIGx2AUchB",
			"type": "image",
			"x": 391.51309260284006,
			"y": 949.5078392240612,
			"width": 933,
			"height": 216,
			"angle": 0,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 466095243,
			"version": 66,
			"versionNonce": 597309515,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "tW_-yjabtbHCtevauXXbF",
					"type": "arrow"
				}
			],
			"updated": 1708910671008,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "73b296aa34d21e4f661ea8e5123ef46ef6219391",
			"scale": [
				1,
				1
			]
		},
		{
			"id": "tW_-yjabtbHCtevauXXbF",
			"type": "arrow",
			"x": -35.986907397159484,
			"y": 1033.5078392240612,
			"width": 405.9999999999998,
			"height": 2,
			"angle": 0,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 1472596069,
			"version": 69,
			"versionNonce": 1407383275,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1708910672232,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					405.9999999999998,
					-2
				]
			],
			"lastCommittedPoint": null,
			"startBinding": null,
			"endBinding": {
				"elementId": "Z-Cox0eI_-jKIGx2AUchB",
				"focus": 0.25751993032759435,
				"gap": 21.499999999999773
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "dVHrlLdY",
			"type": "text",
			"x": -43.432219481014386,
			"y": 1203.1968688997922,
			"width": 10,
			"height": 25,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 468166725,
			"version": 11,
			"versionNonce": 302330053,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1708909480821,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 18,
			"containerId": null,
			"originalText": "",
			"lineHeight": 1.25
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
		"currentItemFontSize": 36,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 316.51860250303616,
		"scrollY": -349.5171860085728,
		"zoom": {
			"value": 0.9622675815785541
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