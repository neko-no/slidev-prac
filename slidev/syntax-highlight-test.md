# シンタックスハイライト検知テスト

このファイルはSlidevでシンタックスハイライトが正常に動作するかをテストするためのものです。

## JavaScript
```javascript
function greet(name) {
  const message = `Hello, ${name}!`;
  console.log(message);
  return message;
}

// ES6のアロー関数
const add = (a, b) => a + b;

// Promise使用例
async function fetchData() {
  try {
    const response = await fetch('/api/data');
    const data = await response.json();
    return data;
  } catch (error) {
    console.error('Error:', error);
  }
}
```

## TypeScript
```typescript
interface User {
  id: number;
  name: string;
  email: string;
  isActive?: boolean;
}

class UserService {
  private users: User[] = [];

  addUser(user: User): void {
    this.users.push(user);
  }

  findUser(id: number): User | undefined {
    return this.users.find(user => user.id === id);
  }

  getActiveUsers(): User[] {
    return this.users.filter(user => user.isActive ?? true);
  }
}

// ジェネリクス使用例
function identity<T>(arg: T): T {
  return arg;
}
```

## Python
```python
import asyncio
from typing import List, Dict, Optional

class DataProcessor:
    def __init__(self, name: str):
        self.name = name
        self.data: List[Dict] = []
    
    def process_data(self, items: List[str]) -> Dict[str, int]:
        """データを処理して統計を返す"""
        result = {}
        for item in items:
            result[item] = result.get(item, 0) + 1
        return result
    
    async def fetch_remote_data(self, url: str) -> Optional[Dict]:
        """リモートデータを非同期で取得"""
        try:
            # 実際のHTTPリクエスト処理
            await asyncio.sleep(1)  # 模擬的な遅延
            return {"status": "success", "data": [1, 2, 3]}
        except Exception as e:
            print(f"Error fetching data: {e}")
            return None

# リスト内包表記
squares = [x**2 for x in range(10) if x % 2 == 0]

# デコレータ使用例
def timer(func):
    def wrapper(*args, **kwargs):
        import time
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} took {end - start:.2f} seconds")
        return result
    return wrapper
```

## Java
```java
import java.util.*;
import java.util.stream.Collectors;

public class DataManager {
    private final Map<String, Object> cache = new HashMap<>();
    private final List<String> history = new ArrayList<>();
    
    public Optional<Object> getData(String key) {
        history.add(key);
        return Optional.ofNullable(cache.get(key));
    }
    
    public void setData(String key, Object value) {
        cache.put(key, value);
    }
    
    // ストリームAPI使用例
    public List<String> getRecentHistory(int limit) {
        return history.stream()
            .skip(Math.max(0, history.size() - limit))
            .collect(Collectors.toList());
    }
    
    // ジェネリクスとワイルドカード
    public <T extends Comparable<T>> T findMax(List<T> items) {
        return items.stream()
            .max(T::compareTo)
            .orElse(null);
    }
}

// レコード（Java 14+）
public record Person(String name, int age, String email) {
    public Person {
        if (age < 0) {
            throw new IllegalArgumentException("Age cannot be negative");
        }
    }
    
    public boolean isAdult() {
        return age >= 18;
    }
}
```

## CSS/SCSS
```css
/* CSS変数とFlexbox */
:root {
  --primary-color: #3498db;
  --secondary-color: #2ecc71;
  --font-size: 16px;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
}

/* CSS Grid */
.grid-layout {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1rem;
  padding: 2rem;
}

/* メディアクエリ */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
    padding: 1rem;
  }
}

/* アニメーション */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.fade-in {
  animation: fadeIn 0.5s ease-in-out;
}
```

```scss
// SCSS例
$primary: #3498db;
$secondary: #2ecc71;

@mixin button-style($bg-color, $text-color: white) {
  background-color: $bg-color;
  color: $text-color;
  padding: 0.5rem 1rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  
  &:hover {
    background-color: darken($bg-color, 10%);
  }
}

.btn-primary {
  @include button-style($primary);
}

.btn-secondary {
  @include button-style($secondary);
}
```

## HTML
```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>シンタックスハイライトテスト</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="header">
    <nav class="nav">
      <ul class="nav-list">
        <li><a href="#home">ホーム</a></li>
        <li><a href="#about">について</a></li>
        <li><a href="#contact">お問い合わせ</a></li>
      </ul>
    </nav>
  </header>
  
  <main class="main">
    <section class="hero">
      <h1>Welcome to Our Site</h1>
      <p>This is a sample HTML document for testing syntax highlighting.</p>
      <button onclick="handleClick()" class="btn btn-primary">
        クリックしてください
      </button>
    </section>
    
    <section class="content">
      <article class="post">
        <h2>記事タイトル</h2>
        <time datetime="2024-01-01">2024年1月1日</time>
        <p>記事の内容がここに入ります。</p>
      </article>
    </section>
  </main>
  
  <footer class="footer">
    <p>&copy; 2024 Test Site. All rights reserved.</p>
  </footer>
  
  <script src="script.js"></script>
</body>
</html>
```

## JSON
```json
{
  "name": "syntax-highlight-test",
  "version": "1.0.0",
  "description": "A test file for syntax highlighting",
  "main": "index.js",
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js",
    "test": "jest",
    "build": "webpack --mode=production"
  },
  "dependencies": {
    "express": "^4.18.0",
    "lodash": "^4.17.21",
    "moment": "^2.29.4"
  },
  "devDependencies": {
    "nodemon": "^2.0.20",
    "jest": "^29.0.0",
    "webpack": "^5.74.0"
  },
  "keywords": ["test", "syntax", "highlighting"],
  "author": "Developer",
  "license": "MIT",
  "repository": {
    "type": "git",
    "url": "https://github.com/example/syntax-highlight-test.git"
  }
}
```

## YAML
```yaml
# Docker Compose設定例
version: '3.8'

services:
  web:
    image: nginx:alpine
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - ./html:/usr/share/nginx/html
      - ./nginx.conf:/etc/nginx/nginx.conf
    environment:
      - NGINX_HOST=localhost
      - NGINX_PORT=80
    depends_on:
      - api

  api:
    build:
      context: ./api
      dockerfile: Dockerfile
    ports:
      - "3000:3000"
    environment:
      - NODE_ENV=production
      - DATABASE_URL=mongodb://db:27017/myapp
    volumes:
      - ./api:/app
      - /app/node_modules
    depends_on:
      - db

  db:
    image: mongo:latest
    ports:
      - "27017:27017"
    volumes:
      - mongodb_data:/data/db
    environment:
      - MONGO_INITDB_ROOT_USERNAME=admin
      - MONGO_INITDB_ROOT_PASSWORD=password

volumes:
  mongodb_data:

networks:
  default:
    driver: bridge
```

## SQL
```sql
-- データベース作成とテーブル定義
CREATE DATABASE IF NOT EXISTS test_db;
USE test_db;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL UNIQUE,
    email VARCHAR(100) NOT NULL UNIQUE,
    password_hash VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    is_active BOOLEAN DEFAULT TRUE,
    INDEX idx_username (username),
    INDEX idx_email (email)
);

CREATE TABLE posts (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT NOT NULL,
    title VARCHAR(200) NOT NULL,
    content TEXT,
    status ENUM('draft', 'published', 'archived') DEFAULT 'draft',
    published_at TIMESTAMP NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE
);

-- 複雑なクエリ例
SELECT 
    u.username,
    u.email,
    COUNT(p.id) as post_count,
    AVG(LENGTH(p.content)) as avg_content_length,
    MAX(p.published_at) as last_published
FROM users u
LEFT JOIN posts p ON u.id = p.user_id AND p.status = 'published'
WHERE u.is_active = TRUE
    AND u.created_at >= DATE_SUB(NOW(), INTERVAL 1 YEAR)
GROUP BY u.id, u.username, u.email
HAVING post_count > 0
ORDER BY post_count DESC, u.username ASC
LIMIT 10;

-- ストアドプロシージャ
DELIMITER //
CREATE PROCEDURE GetUserStats(IN user_id INT)
BEGIN
    DECLARE done INT DEFAULT FALSE;
    DECLARE post_count INT;
    
    SELECT COUNT(*) INTO post_count 
    FROM posts 
    WHERE user_id = user_id AND status = 'published';
    
    IF post_count > 0 THEN
        SELECT 
            username,
            email,
            post_count,
            created_at
        FROM users 
        WHERE id = user_id;
    ELSE
        SELECT 'No published posts found' as message;
    END IF;
END //
DELIMITER ;
```

## Bash/Shell
```bash
#!/bin/bash

# 設定変数
PROJECT_NAME="syntax-highlight-test"
BUILD_DIR="./build"
LOG_FILE="/var/log/${PROJECT_NAME}.log"

# 関数定義
log_message() {
    local level=$1
    local message=$2
    echo "$(date '+%Y-%m-%d %H:%M:%S') [$level] $message" | tee -a "$LOG_FILE"
}

check_dependencies() {
    local deps=("node" "npm" "git")
    for dep in "${deps[@]}"; do
        if ! command -v "$dep" &> /dev/null; then
            log_message "ERROR" "$dep is not installed"
            return 1
        fi
    done
    log_message "INFO" "All dependencies are available"
    return 0
}

# メイン処理
main() {
    log_message "INFO" "Starting build process for $PROJECT_NAME"
    
    # 依存関係チェック
    if ! check_dependencies; then
        log_message "ERROR" "Dependency check failed"
        exit 1
    fi
    
    # ビルドディレクトリの準備
    if [ -d "$BUILD_DIR" ]; then
        log_message "INFO" "Cleaning existing build directory"
        rm -rf "$BUILD_DIR"
    fi
    
    mkdir -p "$BUILD_DIR"
    
    # ビルド実行
    log_message "INFO" "Running build..."
    if npm run build 2>&1 | tee -a "$LOG_FILE"; then
        log_message "SUCCESS" "Build completed successfully"
    else
        log_message "ERROR" "Build failed"
        exit 1
    fi
    
    # 結果の確認
    if [ -d "$BUILD_DIR" ] && [ "$(ls -A $BUILD_DIR)" ]; then
        log_message "INFO" "Build artifacts created in $BUILD_DIR"
        ls -la "$BUILD_DIR"
    else
        log_message "WARNING" "Build directory is empty"
    fi
}

# スクリプト実行
if [[ "${BASH_SOURCE[0]}" == "${0}" ]]; then
    main "$@"
fi
```

このファイルには主要なプログラミング言語のシンタックスハイライトテスト用のコード例が含まれています。Slidevでプレゼンテーション時に各言語のハイライトが正しく表示されるかを確認できます。