## ✅ Added Parsers and Custom Directive

### 📦 ByteSize Parser
- Parses inputs like `1KB`, `1.5MB`, `10GB`
- Converts them to `ByteSize` objects (for size-related operations)

### ⏱ TimeDuration Parser
- Parses values like `100ms`, `2s`, `5min`, `1h`
- Converts them to `TimeDuration` objects (for time-related processing)

---

### 🧮 New Directive: `aggregate-stats`

**Purpose:**  
Sums up total byte size and time duration from the input records.

**Syntax:**

**Example:**

**Input:**

| size  | time |
|-------|------|
| 1MB   | 2s   |
| 512KB | 3s   |

**Output:**

| total_size_mb | total_time_sec |
|---------------|----------------|
| 1.5           | 5.0            |

---

### 🔧 Files Modified or Added
- `Directives.g4`
- `RecipeVisitor.java`
- `utils/ByteSize.java`
- `utils/TimeDuration.java`
- `steps/AggregateStats.java`
- `AggregateStatsTest.java`
- `README.md`
