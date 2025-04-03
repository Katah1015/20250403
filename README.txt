Blueprint Interface 사용
BP_MoveLeftRight : 좌우로 반복해서 움직이는 박스
BP_MoveRect : 오른쪽->위->왼쪽->아래로 움직이는 박스
BP_Timer : Hud화면 상단 중앙에 00:00 시간 축력하는 액터
BP_Coin : 5개 배치 후 먹을때 마다 Hud화면 오른쪽 하단에 Coin 카운트 증가
BP_Switch : BeginOverlap하면 BP_MoveLeftRight, BP_MoveRect, BP_Timer가 움직이고  EndOverlap하면 BP_MoveLeftRight, BP_MoveRect, BP_Timer가 멈추는 액터
------------------------------------------------------------------------------------------
EventDispatcher 사용
BP_MoveLeftRight_Delegate : 좌우로 반복해서 움직이는 박스 BP_Switch_Delegate에 BeginOverlap하면 움직이고 EndOverlap하면 정지
BP_MoveRect_Delegate : 오른쪽->위->왼쪽->아래로 움직이는 박스 BP_Switch_Delegate에 BeginOverlap하면 움직이고 EndOverlap하면 정지
BP_CountBox_Delegate : BP_Switch_Delegate에 오버랩할때 마다 박스위에 카운트가 증가 9이상이면 다시 0으로 초기화 됩니다.(0~9)
BP_Cannon, BP_Bullet : BP_Cannon에서 BP_Bullet이 1초마다 스폰 된다. BP_Switch_Delegate에 BeginOverlap하면 움직이고 EndOverlap하면 정지
BP_Switch_Delegate : BeginOverlap하면 BP_MoveLeftRight, BP_MoveRect, BP_Timer가 움직이고 
    EndOverlap하면 BP_MoveLeftRight, BP_MoveRect, BP_Timer가 멈추는 액터