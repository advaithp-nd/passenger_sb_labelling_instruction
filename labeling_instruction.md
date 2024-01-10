# Introduction
Passenger Seatbelt compliance alert is raised whenever passenger is detected without a seatbelt.
 
# Feature Definition and Event Codes
 
| Event Code | Description                                |
|:------------|:------------------------------------------:|
| 100.0.1     | Passenger not wearing Seatbelt             |
| 100.1.3.2     | Passenger not wearing Seatbelt (Speed based - Amazon only) |
 
For all labelling purposes, both 100.0.1 and 100.1.3.2 should be treated similarly. 
> Passenger seatbelt compliance is currently disabled
 
### GENERIC TAGS:
These tags can be used on both Valid and Invalid labeled videos if they are relevant.
 
#### PHONE_OCCLUSION
This tag will be used if a mounted phone is occluding the passenger and preventing you from seeing the passenger's torso (upper body) completely or partially. 

**PhoneOcclusion** . 
 *Video examples given below are of driver seatbelt case , Beacuse passenger seatbelt examples are not available . 

* https://analytics-kpis.netradyne.com/video?aaid=d215aa26-874c-49a4-a446-5fa4c3453067
* https://analytics-kpis.netradyne.com/video?aaid=631be002-dc84-42af-b72e-ad0e0071c52a
* https://analytics-kpis.netradyne.com/video?aaid=a832a8a2-0a7c-4ff2-b140-7aa90b29144a
* https://analytics-kpis.netradyne.com/video?aaid=b22e3b37-7b7a-4d8e-ac2f-cb10c9ac68f4
* https://analytics-kpis.netradyne.com/video?avid=21607f63-3802-4351-b0f6-c2fa8d8768f1


#### WAIST_BELT_NOT_VISIBLE
This will be used when the waist belt of the passenger is not visible. This is usually because the camera angle or the FOV is not exposing the waist of the driver. This tag can also be used with the BAD_FOV tag.

 **WaistBeltNotVisible**

* https://analytics-kpis.netradyne.com/video?avid=034ff514-a83e-4bcd-bc94-f35d3ed41c63 DAY

#### DETECTED_MULTIPLE_PASSENGER

When the green bounding box is detecting multiple passengers during the alert.
*Video examples given below are of driver seatbelt case , Beacuse passenger seatbelt examples are not available . 

* https://analytics-kpis.netradyne.com/video?aaid=88d517c4-7652-431a-9972-55aff5d180dd 
	
#### NIGHT
When the Infrared Lights are on. This can be determined by a purple light that’s reflected on the driver or in the vehicle. 

#### PASSENGER_STANDING
When passenger is standing in the vehicle
	
#### VIDEO_STUTTERING 
The video is skipping and not providing a smooth play through.
 
* https://analytics-kpis.netradyne.com/video?aaid=f1fcceae-7c04-4889-b3f2-418c24a53507
	
#### MOUNT_ISSUE_PRESENT 
Face is looking sideways because of position of device mount.
*Video examples given below are of driver seatbelt case , Beacuse passenger seatbelt examples are not available . 
* https://analytics-kpis.netradyne.com/video?aaid=3cef7a9b-06f2-422d-b9d5-bd8c42d0936f

### FEATURE TAGS:
 
### Valid Examples
Whenever a passenger is not wearing a seatbelt or is wearing their seatbelt incorrectly, an alert should be raised. The tags below will be used exclusively for Valid labeled videos. 

* https://analytics-kpis.netradyne.com/video?avid=45c49790-ffe9-4d24-912c-ba659a20d0b0
* https://analytics-kpis.netradyne.com/video?avid=31bafce9-78f6-4606-83cb-c16d38c40d91


 
#### SEATBELT_STATUS_CHANGED
This tag will be used if the passenger did not originally have their seatbelt on and is seen putting on their seatbelt in the video. 
*Video examples given below are of driver seatbelt case , Beacuse passenger seatbelt examples are not available . 
* https://analytics-kpis.netradyne.com/video?aaid=d1c19383-0e2d-4998-8f57-1d01f36eb1e3
* https://analytics-kpis.netradyne.com/video?aaid=de29d7d2-1597-47dd-b263-6c0f67a94e3e
* https://analytics-kpis.netradyne.com/video?aaid=d78d3ff1-b8ed-496a-9760-1bf32caa9a35

#### LOOSE_SEATBELT
If the seatbelt is loose around the upper body. Tag the corresponding false alerts as **LooseSeatbelt**
* https://analytics-kpis.netradyne.com/video?avid=d15d5175-09c4-440d-a8b1-6bbc81276458
* https://analytics-kpis.netradyne.com/video?avid=8d6d3b44-3b5f-4608-862e-d8fd637f4ea5


#### WEARING_WRONG
If the seatbelt is not worn properly. The passenger is wearing their seatbelt in a non-conventional (uncommon) way. A common example you might see is when the driver is wearing their seatbelt under the arm etc. If an alert is raised in such cases, tag the corresponding false alerts as 
**WearingWrong**
*Video examples given below are of driver seatbelt case , Beacuse passenger seatbelt examples are not available . 
* https://analytics-kpis.netradyne.com/video?aaid=374d282b-0d5f-4dcc-9d90-52d9d6a0acf2
* https://analytics-kpis.netradyne.com/video?aaid=20222a4f-a0ff-4441-8204-65a27ee8d8c2  - IR
* https://analytics-kpis.netradyne.com/video?aaid=1a1d078e-4682-44f3-9a13-e424201baa5d  - Day
* https://analytics-kpis.netradyne.com/video?aaid=f7e3c836-0f90-42a1-a425-f5d436484eb4  - IR

#### WAIST_BELT_NOT_WORN
This tag will be used when we are able to see the waist of the driver AND the belt that normally crosses over the waist is not properly worn. A common scenario that you may come across for this tag is when the passenger only has the shoulder strap of the seatbelt on and sitting on the waist strap. Below are a few examples for this tag. **WaistBeltNotWorn**
* https://analytics-kpis.netradyne.com/video?avid=10a3d0ee-9024-4d68-917d-755e104436b9


### Invalid Examples
Whenever a passenger is wearing a seatbelt, but an alert was raised. The tags below will be used exclusively for Invalid labeled videos. 
 
#### PARTIAL_SEATBELT_OCCLUDED
Sometimes the seatbelt can be slightly occluded by objects in front of the passenger. This can range from the passenger's arm covering a portion of the seatbelt, to clothing, or any object that would only partially cover the seatbelt of the passenger. Tag these invalid scenarios as **PartialSeatbeltOccluded**
* https://analytics-kpis.netradyne.com/video?avid=ebb3950e-a02b-4afd-bb4e-6db8dd0921bf
* https://analytics-kpis.netradyne.com/video?avid=080c234f-56dd-4b73-b20d-a1b3a361af35

 
#### COMPLETE_SEATBELT_OCCLUDED
If most of the seatbelt region on the passenger's torso/upper body is not visible. Tag these invalid scenarios as **CompleteSeatbeltOccluded**
* https://analytics-kpis.netradyne.com/video?avid=ec062f7a-44c6-41f1-ab66-11817d4f7c77
* https://analytics-kpis.netradyne.com/video?avid=b71ab871-e4f4-4994-8352-8bf3c9695b77


#### SIMILAR_SHIRT_COLOR
This tag will be used when the color of the seatbelt and the passenger's clothes are very similar. 
Due to low contrast along with the seatbelt color being like the color of the passenger's clothes, the model fails to detect the seatbelt. Tag the corresponding false alerts as **SimilarShirtColor**
* https://analytics-kpis.netradyne.com/video?avid=d84e3210-99dc-444c-9c24-c5903773eeae 
* https://analytics-kpis.netradyne.com/video?avid=14082d1c-acaf-47ee-8185-0bd6a7b838d5
* https://analytics-kpis.netradyne.com/video?avid=b55a23df-6597-42d5-a578-9b53ba63e0c5
* https://analytics-kpis.netradyne.com/video?avid=d84e3210-99dc-444c-9c24-c5903773eeae

#### SATURATED_TORSO
If the seatbelt or the torso/upper body is saturated (image becomes washed out/white) due to sunlight or IR light, Tag the corresponding false alerts as **SaturatedTorso**
* https://analytics-kpis.netradyne.com/video?avid=034ff514-a83e-4bcd-bc94-f35d3ed41c63 
* https://analytics-kpis.netradyne.com/video?avid=19bcc3f3-e5f1-4d99-8809-bcf9aa362995
* https://analytics-kpis.netradyne.com/video?avid=e9bad26e-9e46-4fd4-aaae-bbaf836a5132
* https://analytics-kpis.netradyne.com/video?avid=Day 3a98576f-56c8-40b6-8673-667e0580b380

#### BAD_FOV
If the passenger's torso/upper body is not completely inside the frame or not enough torso is visible either horizontally (both shoulders should be visible) or vertically (at least 75% of the upperbody should be visible) , Tag the corresponding false alerts as **BadFOV**

* https://analytics-kpis.netradyne.com/video?aaid=6feb3137-d974-4b2a-92d6-40bd9eeb2a2a  - Horizontally low FOV
* https://analytics-kpis.netradyne.com/video?aaid=8295d631-3481-4d71-a5a2-f110d9993986  - Vertically low FOV
* https://analytics-kpis.netradyne.com/video?aaid=47e62f8e-b586-4e0f-ae6d-76b6d6424976  - Horizontally low FOV

#### BAD_LIGHTING
Bad lightening (Dark, low light) can cause the seatbelt to look blurry or become less visible. Tag as **BadLighting**
* https://analytics-kpis.netradyne.com/video?aaid=c4f8aa1b-4a22-4a01-851c-db2c6b3f3d72
* https://analytics-kpis.netradyne.com/video?aaid=2cb1fdc0-5fa1-4376-a331-5c76c2cdafd9
* https://analytics-kpis.netradyne.com/video?aaid=50e9178c-b4e9-46cf-9476-565cf1051e7b
* https://analytics-kpis.netradyne.com/video?aaid=4f1dfabc-245a-48c1-b9e1-f9a50223dd2f   - IR

#### VISIBLE_SEATBELT
If none of the above are the reasons for failure and seatbelt is seen clearly and an alert is generated, tag the false alerts as **VisibleSeatbelt**
* https://analytics-kpis.netradyne.com/video?avid=c2e4e829-febe-4c07-a3ea-59e20be1e13c
* https://analytics-kpis.netradyne.com/video?avid=2f050d79-29d7-41bb-9886-ebfdf149da37

#### VEHICLE_STATIONARY
The passenger is not-wearing seatbelt but the vehicle is not moving at alert start time. Tag as **VehicleStationary**.
* https://analytics-kpis.netradyne.com/video?aaid=dbe19b1c-7a00-4cb4-9965-2326458e4ecb
* https://analytics-kpis.netradyne.com/video?aaid=8ad3e5da-06a4-4ce2-83ec-429f4360c124
* https://analytics-kpis.netradyne.com/video?aaid=982450e4-0d5b-4b6b-9b7d-d3614124e4ac
* https://analytics-kpis.netradyne.com/video?aaid=412e2e00-caa5-4ed3-a4f9-336aeccf4878
 
#### SPEED_NOT_AVAILABLE
The speed is not displayed on the video, and hence cannot determine if vehicle is moving above the speed threshold. Tag as **SpeedNotAvailable**.
In these cases, the labelers should also add additional tag indicating the seatbelt status mentioned above.
* https://analytics-kpis.netradyne.com/video?aaid=3d44287a-a58a-41b5-b95f-9929286a00fb
 
#### INSUFFICIENT_CONTEXT
The alert start timestamp is outside the video duration interval. Tag as **InsufficientContext**.
* https://analytics-kpis.netradyne.com/video?aaid=4f751af9-5731-43ce-a22c-420728b7c6ec

#### PASSENGER_NOT_PRESENT_PASSENGER_SEAT_EMPTY
Passenger is not present. Wrongly detecting passenger box on 'passenger seat'. No objects present in passenger seat .  

#### PASSENGER_NOT_PRESENT_HOODIE_PRESENT_IN_PASSENGER_SEAT
Passenger is not present. Wrongly detecting passenger box on 'passenger seat'. Hoodie is on passenger seat . Hoodie is placed on passenger seat sunch a way that it looks similar to person wearing hoodie . 
* https://analytics-kpis.netradyne.com/video?avid=968a75f4-6b38-4cd7-806a-292155a91ce7 :Day
* https://analytics-kpis.netradyne.com/video?avid=961d8f61-22f7-40e8-a1c6-9f562e0e8166 :IR 
* https://analytics-kpis.netradyne.com/video?avid=912a9a54-adc4-4ce6-b176-fdc1b4a6fb94 :IR
* https://analytics-kpis.netradyne.com/video?avid=08f47e48-1000-45e9-a4c0-e02e39363a2f  :IR 


#### PASSENGER_NOT_PRESENT_OTHER_OBEJCTS_PRESENT_IN_PASSENGER_SEAT
Passenger is not present. Wrongly detecting passenger box on 'passenger seat'. Hoodie is on passenger seat . 
* https://analytics-kpis.netradyne.com/video?avid=2aeb43ee-d5b0-4997-91f6-3efe19bad446 :IR 
* https://analytics-kpis.netradyne.com/video?avid=e4b38535-9981-4fc5-a1c1-58c5dc3e449a :IR 
* https://analytics-kpis.netradyne.com/video?avid=4c778aed-876f-46c8-9e4d-5f109533267e :Day
* https://analytics-kpis.netradyne.com/video?avid=2016d957-af81-4170-992c-c332f3bc432c :Day


