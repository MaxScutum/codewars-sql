# CodeWars SQL Solutions 7 kyu SQL.

---

SQL Basics: Create a FUNCTION

Description:

For this challenge you need to create a basic Increment function which Increments on the age field of the peoples table.

The function should be called `increment`, it needs to take 1 integer and increment that number by 1.

You may query the people table while testing but the query must only contain the function on your final submit.

important: you must remove all comments when submitting the kata.

people table schema

```text
id
name
age
```

NOTE: Your solution should use PL/SQL. Ruby is used within the test cases to do the actual testing.

---

### Given Code

```sql
-- Create your function here
```

---

### Solution

```sql
CREATE FUNCTION increment(i integer) RETURNS integer AS $$
BEGIN
  RETURN i + 1;
END;
$$ LANGUAGE plpgsql;
```

---

### Tests

```ruby
results = run_sql

describe "tests" do
  describe "should contain keywords" do
    it "should contain CREATE" do
      expect($sql.upcase).to include("CREATE")
    end

    it "should contain FUNCTION" do
      expect($sql.upcase).to include("FUNCTION")
    end

    it "should contain increment" do
      expect($sql.upcase).to include("INCREMENT")
    end

    it "should not query people table" do
      expect($sql.upcase).not_to include("PEOPLE")
    end
  end
end
```

---

[See on CodeWars.com](https://www.codewars.com/kata/580fe518cefeff16d00000c0)
