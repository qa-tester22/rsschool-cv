# Laura Bright

Software engineer in Test | Cypress Ambassador  

---

## Contact information:

- Phone: +44 7857 006916
- E-mail: wavenlondon@gmail.com
- Telegram: @qa_tester22

---

## About Myself:

Cypress ambassador | Software Automation Quality Assurance Engineer | JavaScript Cypress HTML CSS | node.js | We're here to ensure your software works flawlessly | Comprehensive testing at a price that suits you

---

## Skills and Proficiency:

- Javascript | Html | CSS | XML
- Cypress | Jest | 
- Git | GitHub | Docker | Jenkins
- SQL | PosgeSQL | non-SQL | MySQL
- Percy | Charles 

---

## Code example:

---

**Задача**
Пользователь может выбрать количества картинок на веб-сайте от 5 до 10 (пагинация)

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Pagination Example</title>
    <style>
        .pagination {
            display: flex;
            list-style: none;
            padding: 0;
        }
        .pagination li {
            margin: 0 5px;
            padding: 5px 10px;
            border: 1px solid #ccc;
            cursor: pointer;
        }
        .pagination li.active {
            background-color: #007bff;
            color: white;
        }
        .pagination li:hover {
            background-color: #ddd;
        }
        .image-wrapper {
            display: flex;
            flex-wrap: wrap;
        }
        .image-wrapper img {
            margin: 10px;
            width: 100px;
            height: 100px;
            object-fit: cover;
        }
        .control {
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div class="control">
        <label for="itemsPerPage">Images per page:</label>
        <select id="itemsPerPage" onchange="updateItemsPerPage()">
            <option value="5">5</option>
            <option value="6">6</option>
            <option value="7">7</option>
            <option value="8">8</option>
            <option value="9">9</option>
            <option value="10">10</option>
        </select>
    </div>
    <div id="content" class="image-wrapper"></div>
    <ul id="pagination" class="pagination"></ul>

    <script>
        // Sample data (array of image URLs)
        const items = Array.from({ length: 50 }, (_, i) => `https://picsum.photos/200/200?random=${i + 1}`);

        // Pagination variables
        let itemsPerPage = 5;
        let currentPage = 1;

        // Function to display items
        function displayItems(items, wrapper, rowsPerPage, page) {
            wrapper.innerHTML = "";
            page--;

            const start = rowsPerPage * page;
            const end = start + rowsPerPage;
            const paginatedItems = items.slice(start, end);

            paginatedItems.forEach(item => {
                const imgElement = document.createElement("img");
                imgElement.src = item;
                wrapper.appendChild(imgElement);
            });
        }

        // Function to setup pagination buttons
        function setupPagination(items, wrapper, rowsPerPage) {
            wrapper.innerHTML = "";

            const pageCount = Math.ceil(items.length / rowsPerPage);
            for (let i = 1; i < pageCount + 1; i++) {
                const btn = paginationButton(i, items);
                wrapper.appendChild(btn);
            }
        }

        // Function to create pagination buttons
        function paginationButton(page, items) {
            const button = document.createElement("li");
            button.textContent = page;

            if (currentPage === page) button.classList.add("active");

            button.addEventListener("click", () => {
                currentPage = page;
                displayItems(items, document.getElementById("content"), itemsPerPage, currentPage);

                const currentBtn = document.querySelector(".pagination li.active");
                if (currentBtn) currentBtn.classList.remove("active");

                button.classList.add("active");
            });

            return button;
        }

        // Function to update items per page
        function updateItemsPerPage() {
            itemsPerPage = parseInt(document.getElementById("itemsPerPage").value);
            currentPage = 1;
            displayItems(items, document.getElementById("content"), itemsPerPage, currentPage);
            setupPagination(items, document.getElementById("pagination"), itemsPerPage);
        }

        // Initialize the pagination
        displayItems(items, document.getElementById("content"), itemsPerPage, currentPage);
        setupPagination(items, document.getElementById("pagination"), itemsPerPage);
    </script>
</body>
</html>

```

---

## Languages

- Russian - native speaker
- some tech languges 
- English - B2 | C1
