# BÁO CÁO CÁ NHÂN DỰ ÁN 8-PUZZLE AI

## 1. Mục tiêu

Mục tiêu của project là áp dụng các nhóm thuật toán AI khác nhau để giải bài toán 8-puzzle (trò chơi 8 ô chữ) và so sánh hiệu suất giữa chúng. Qua đó, em hiểu rõ hơn cách các thuật toán tìm kiếm hoạt động và hiệu quả của chúng trong việc giải quyết một bài toán cụ thể.

## 2. Nội dung

### 2.1. Các thuật toán Tìm kiếm không có thông tin (Uninformed Search)

**Thuật toán sử dụng:**
- BFS (Breadth-First Search)
- DFS (Depth-First Search)
- UCS (Uniform Cost Search)
- IDDFS (Iterative Deepening Depth-First Search)

**Các thành phần chính của bài toán tìm kiếm:**
- **State:** vị trí hiện tại của các ô số.
- **Initial state:** trạng thái ban đầu do người dùng nhập hoặc tạo ngẫu nhiên.
- **Goal state:** trạng thái đích chuẩn `[1,2,3,4,5,6,7,8,0]`.
- **Actions:** di chuyển ô trống lên/xuống/trái/phải.
- **Transition model:** thực hiện hành động sẽ tạo ra trạng thái mới.
- **Path cost:** tính bằng số bước di chuyển (với UCS thì trọng số có thể bằng 1 cho mỗi bước).
- **Giải pháp (solution):** là chuỗi các hành động dẫn từ trạng thái bắt đầu đến trạng thái mục tiêu.

**Minh họa:**
- (GIF mô phỏng BFS, DFS, UCS, IDDFS giải bài toán - em sẽ chèn ở đây các hình ảnh động nếu có.)
- (Biểu đồ so sánh số nút đã duyệt, độ sâu, thời gian thực thi.)

**Nhận xét:**
- BFS luôn tìm ra đường đi ngắn nhất nhưng tốn bộ nhớ.
- DFS có thể bị lặp và không tối ưu.
- UCS hiệu quả nếu chi phí hành động khác nhau (ở đây giống BFS).
- IDDFS kết hợp được ưu điểm của DFS và BFS nhưng mất thời gian do duyệt lại nhiều lần.

---

### 2.2. Các thuật toán Tìm kiếm có thông tin (Informed Search)

**Thuật toán sử dụng:**
- A* Search
- IDA* (Iterative Deepening A*)
- Greedy Best-First Search

**Heuristic dùng:**
- Số ô sai vị trí (Misplaced Tiles)
- Tổng khoảng cách Manhattan

**Trình bày tương tự 2.1:**
- (GIF mô phỏng A*, IDA*, Greedy)
- (Biểu đồ hiệu suất, số nút duyệt, thời gian)

**Nhận xét:**
- A* rất mạnh, tìm được đường đi tối ưu nhanh chóng.
- Greedy tìm nhanh nhưng không tối ưu.
- IDA* tiết kiệm bộ nhớ hơn A* nhưng chậm hơn.

---

### 2.3. Tìm kiếm cục bộ (Local Search)

**Thuật toán sử dụng:**
- Simple Hill Climbing
- Steepest Ascent Hill Climbing
- Stochastic Hill Climbing
- Simulated Annealing
- Beam Search
- Genetic Algorithm

**Giải pháp:** là trạng thái mục tiêu được tiếp cận bằng cách cải tiến dần từ trạng thái hiện tại.

**Nhận xét:**
- Hill climbing dễ bị kẹt ở cực trị cục bộ.
- Simulated Annealing đôi khi thoát được.
- Genetic Algorithm thú vị nhưng khó điều chỉnh.
- Beam Search khá hiệu quả nếu chọn số chùm thích hợp.

---

### 2.4. Tìm kiếm trong môi trường phức tạp

**Thuật toán sử dụng:**
- And-Or Search
- Belief State
- Search with Partial Observation

**Nhận xét:**
- Không áp dụng mạnh cho 8-puzzle vì đây là bài toán xác định và quan sát đầy đủ.
- Tuy nhiên, triển khai để hiểu cách hoạt động.

---

### 2.5. Tìm kiếm trong môi trường có ràng buộc (Constraint-based Search)

**Thuật toán sử dụng:**
- Backtracking
- Generate and Test
- AC-3

**Nhận xét:**
- Không phổ biến cho 8-puzzle nhưng có thể triển khai để thử nghiệm, ví dụ xem mỗi trạng thái có hợp lệ không theo ràng buộc.

---

### 2.6. Reinforcement Learning

**Thuật toán sử dụng:**
- Q-learning
- Reinforcement Learning (Value iteration, Policy iteration)

**Nhận xét:**
- Cần nhiều thời gian để train.
- Q-learning học được chính sách để giải puzzle, tuy chậm nhưng đáng thử.

---

## 3. Kết luận

Qua project này, em đã:
- Hiểu rõ hơn các loại thuật toán AI và cách áp dụng chúng.
- Biết cách xây dựng hàm heuristic và cấu trúc bài toán tìm kiếm.
- Thấy rõ điểm mạnh/yếu của từng nhóm thuật toán.
- Cải thiện kỹ năng lập trình, đặc biệt với Python và việc xử lý trạng thái.

> **Lưu ý:** Các ảnh minh họa sẽ được chèn trong thư mục `/media` hoặc `assets` kèm theo.
