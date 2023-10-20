<!DOCTYPE html>
<html>
<head>
    <title>Admin Panel</title>
</head>
<body>
    <h1>Admin Panel</h1>
    <button id="printButton">Print in Roblox</button>

    <script>
        // JavaScript code
        document.getElementById("printButton").addEventListener("click", function() {
            // Gửi yêu cầu đến trò chơi Roblox khi người dùng nhấn nút
            const request = {
                action: "print" // Thay đổi hành động này tùy theo yêu cầu của bạn
            };

            fetch("https://your-game-api-endpoint.com", {
                method: "POST",
                body: JSON.stringify(request),
                headers: {
                    "Content-Type": "application/json"
                }
            })
            .then(response => response.json())
            .then(data => {
                // Xử lý phản hồi từ trò chơi (nếu có)
                console.log(data);
            })
            .catch(error => {
                console.error(error);
            });
        });
    </script>
</body>
</html>
