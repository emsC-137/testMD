readme
# Report
## TLDR:

## Next:
## Danh sách việc:
<details>
  <summary><h3>Frame</h3></summary>
  <details>
  <summary> Frame chính ✔️</summary>
    <p>  <a href="https://dronenodes.com/drone-frame-racing-freestyle/">Thông số của khung</a></p>
    <ul>
      <li>Kích thước khung: 5 inch (vì được sử dụng rộng rãi và phù hợp cho nhiều mục đích khác nhau.</li>
      <li>Chất liệu: Carbon (Nhẹ và cứng)</li>
      <li>Số cánh: 4 cánh (Số cánh chẵn để dễ cân bằng. 4 là số cánh tối thiểu)</li>
      <li>Layout: Hybrid X (Kết hợp giữa layout H và X. Thân dài hơn -&gt; Chứa được nhiều thiết bị hơn.</li>
    </ul>
    <p>→ Bộ khung sử dụng là One Source V3</p>
  </details>
  
  <details>
  <summary> Khung 3D cho GPS ❌</summary>
  Soon...
  </details>
  
  <details>
  <summary> Khung 3D để giữ Node MCU ❌</summary>
  Soon...
  </details>

</details>

<details>
  <summary><h3>Càng đáp</h3></summary>
  
  <details>
  <summary>Tiêu chí</summary>
  Soon...
  </details>
  
  <details>
  <summary>Thiết kế</summary>
  Soon...
  </details>
  
  <details>
  <summary>Kiểm tra độ cứng vững ❌</summary>
  Soon...
  </details>
</details>

<details>
  <summary><h3>Flight controller</h3></summary>
  
  <details>
  <summary>Yêu cầu tính năng ❌</summary>
  <ul>
      <li>Chạy được ArduPilot</li>
      <li>Có các cảm biến: GYRO, Compass, GPS, Baro</li>
      <li>Có thể kết nối với GCS</li>
      <li>Có các cổng dư để kết nối trong trường hợp thiếu</li>
      <li>Kết nối được với bo nhúng</li>
    </ul>
  </details>
  
  <details>
  <summary>Thông số của FC ✔️</summary>
    <p> FC: <a href="https://nexshop.vn/mamba-dji-f405-mk2-flight-controller-30.530.5mm-p37057191.html">Mamba DJI F405 MK2</a></p>
    <ul>
      <li>GYRO: MPU6000</li>
      <li>Barometer: Yes</li>
      <li>Uarts: 6Set</li>
      <li>Input: 3~6S Lipo (12.6~25.2V)</li>
    </ul>
  </details>
  

</details>

<details>
  <summary><h3>Motor</h3></summary>
  
  <details markdown="1">
  <summary>Glossary ✔️</summary>
   <ul>
      <li>kV</li>
      <p>Là đại lượng được quy ước: X Kv nghĩa là động cơ sẽ xoay với tốc độ X rpm dưới điện áp 1 volt.</p>
      <img src=https://user-images.githubusercontent.com/103067723/178641065-6ecfea47-c529-4dcd-8776-d30d61a64564.png> <br>
      <img src=https://user-images.githubusercontent.com/103067723/178641126-1db040d0-3a88-4e04-ad0b-d8f3962e0656.png>
      <p>Nhìn chung, với Kv càng thấp thì động cơ sẽ tạo torque càng cao.</p>
      <li>Motor size</li>
      <p>Ký hiệu kích thước của stator, được viết dưới dạng XXYY, trong đó XX là bề rộng của stator, còn YY là chiều cao
          YY càng cao, drone sẽ có top speed cao hơn, và điều khiển ở tốc độ thấp khó khăn hơn
          XX càng cao, drone sẽ có top speed thấp hơn, và điều khiển ở tốc độ thấp dễ dàng hơn</p>
    </ul> 
    
  </details>
  
  <details>
  <summary>Chọn motor ✔️</summary>
  <img src=https://user-images.githubusercontent.com/103067723/178643994-f6fc1446-67d6-4324-bfce-2192ba27b931.png>
  <p>Dựa theo bảng hướng dẫn, vì frame ta đang dùng là frame 5 inch, nên chọn motor có kích thước 2204 - 2206; kv 2300-2700 → Chọn motor Performante 2207 - 1750KV Motor AMAXinno T-Bell </p>
  <p>Phần tính toán liên quan đến motor sẽ được đề cập ở mục sau.</p>
  </details>
  
</details>

<details>
  <summary><h3>Cánh quạt</h3></summary>
  
  <ul>
      <li>Ký hiệu ✔️</li>
      <p> L x P x B hoặc LLPP x B (Length, Pitch, số Blade)</p>
      <li>Nhận xét chung ❌</li>
      <p>Cánh quạt có độ vát (pitch) thấp sẽ xoay nhanh hơn, nhưng lực đẩy tiến về phía trước yếu hơn.</p>
      <p>Cánh quạt có độ vát (pitch) cao sẽ có nhiều lực đẩy hơn, đồng nghĩa với tốc độ cao hơn, nhưng điều khiển cũng khó hơn</p>
      <p>Số cánh càng ít thì tốc độ quay càng nhanh, tốn ít năng lượng và hoạt động hiệu quả hơn.</p>
      <p> </p>
  </ul> 
</details>

<details>
  <summary><h3>ESC</h3></summary>
  
  <details>
  <summary>Cách chọn ESC ✔️</summary>
    <p> Ở chế độ max, motor chỉ tốn 80% dòng điện so với mặt đất <a href="https://dronenodes.com/drone-esc-electronic-speed-controller/">Tham Khảo tại đây</a></p>
    <p> Motor max 4S là 40A dưới mặt đất -> 32A trên cao </p>
    <p> Hệ số an toàn giữa ESC và motor nên nằm trong khoảng 1.2 đến 1.5ESC từ 38.4A -> 48A </p>
    <p> Chọn ESC VIVA 45A </p>
  </details>
  
  <details>
  <summary>Thông số của ESC ✔️</summary>
    <p> ESC: <a href="https://www.team-blacksheep.com/products/prod:vivafpv4in1_60a_bl32">VIVA 45A</a></p>
    <ul>
      <li>Input voltage: 3-6S</li>
      <li>Burst current: 60A</li>
      <li>Constant current: 45A</li>
      <li>Input protocols: OneShot42, Multishot, DShot1200</li>
    </ul>
  </details>
  
  <details>
  <summary>Giao thức Dshot ✔️</summary>
    <p> Ưu điểm: </p>
    <ul>
      <li>Ko cần calib ESC</li>
      <li>Chống nhiễu tốt hơn, tín hiệu chính xác hơn</li>
      <li>Resolution = 2048 > 1000 so với các loại khác</li>
      <li>ESC có thể chọn ko đọc các tín hiệu lỗi</li>
    </ul>
    <p> Tốc độ: </p>
    <ul>
      <li>Dshot600 - 600 000 bit/s</li>
      <li>Dshot300</li>
      <li>Dshot150</li>
    </ul>
    <p> 1 package của DShot gồm 16 bit: </p>
    <ul>
      <li>11 bit cho giá trị throttle (2^11 = 2048)</li>
      <ul>
        <li>0 là disarm</li>
        <li>1-47 là special command</li>
        <li>command 0-36 chỉchạy khi motor ko xoay</li>
        <li>48-2048: giá trị throttle</li>
      </ul>
      <li>1 bit telemetry request</li>
      <ul>
        <li>Dùng để yêu cầu 1 thông tin nào đótrảvề cho FC (vd tốcđộ xoay, nhiệtđộ, dòng, áp,..)</li>
        <li>Command số 42-47 là dành cho telemetry</li>
      </ul>
      <li>4 bit check sum</li>
      <ul>
        <li>crc = (value ^ (value >> 4) ^ (value >> 8)) & 0x0F<li>
        <li>IMAGE nhớ chèn</li>
      </ul>
    </ul>
    <p>Thời gian của mỗi frame giống nhau, nhưng hightime của bit 0 và 1 khác nhau</p>
    <p>-> Dễ tính toán duration (= 16 x frame)</p>
    <p>-> Tính giá trị của bit = cách đo từ rising edge và dừng lại ở falling edge</p>
  </details>
  
</details>

<details>
  <summary><h3>GPS</h3></summary>
  
  <details>
  <summary>Soon ✔️</summary>
  Soon...
  </details>
  
  <details>
  <summary>Soon ✔️</summary>
  Soon...
  </details>
  
  <details>
  <summary>Soo ❌</summary>
  Soon...
  </details>
</details>

<details>
  <summary><h3>TX-RX</h3></summary>
  
  <details>
  <summary>Yêu cầu tính năng</summary>
    <ul>
      <li>Kết nối được với FC</li>
      <li>Có nhiều channel cho những mode khác nhau</li>
    </ul>
  </details>
  
  <details>
  <summary>Thông số của TX-RX</summary>
    <p>TX-RX: <a href="https://www.multi-module.org/using-the-module/protocol-details/flysky-afhds2a">FlySky AFHDS 2A</a></p>
    <ul>
      <li>Kết nối với FC bằng SBUS</li>
      <li>Có 10 channel</li>
    </ul>
  </details>
  
</details>

<details>
  <summary><h3>Pin</h3></summary>
  
  <details> 
  <summary>Tính Pin</summary>
    <p>Dựa theo bảng motor, ta có thể chọn 3S/4S với mAh từ 1000-1300mA</p>
    <p>Chọn pin 4S-1550mA-120C</p>
    <p>Motor dùng 32A *4 = 132A</p>
    <p>132/1550 = 85.16C</p>
    <p>-> số C phải lớn hơn 85.16, pin hiện tại C=120</p>
    <p>-> pin đã chọn phù hợp</p>
  </details>
  
</details>

<details>
  <summary><h3>Tỉ số lực đẩy: Khối lượng</h3></summary>
  
  <details>
  <summary>Soon ✔️</summary>
  Soon...
  </details>
  
  <details>
  <summary>Soon ✔️</summary>
  Soon...
  </details>
  
  <details>
  <summary>Soo ❌</summary>
  Soon...
  </details>
</details>

<details>
  <summary><h3>Set up trong ardupilot</h3></summary>
  
  <details>
  <summary>Soon ✔️</summary>
  Soon...
  </details>
  
  <details>
  <summary>Soon ✔️</summary>
  Soon...
  </details>
  
  <details>
  <summary>Soo ❌</summary>
  Soon...
  </details>
</details>

<details>
  <summary><h3>Chỉnh PID lần đầu</h3></summary>
  
  <details>
  <summary>Soon ✔️</summary>
  Soon...
  </details>
  
  <details>
  <summary>Soon ✔️</summary>
  Soon...
  </details>
  
  <details>
  <summary>Soo ❌</summary>
  Soon...
  </details>
</details>
