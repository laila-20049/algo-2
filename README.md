# algo-2
✅ Problem 1: Sum of all distinct elements
pseudo
ALGORITHM distinct_sum
VAR
  set1[4] ← [3, 1, 7, 9]
  set2[5] ← [2, 4, 1, 9, 3]
  sum ← 0
  i, j ← INTEGER
  isCommon ← BOOLEAN
BEGIN
  // Loop for set1
  FOR i FROM 0 TO 3 DO
    isCommon ← FALSE
    FOR j FROM 0 TO 4 DO
      IF set1[i] = set2[j] THEN
        isCommon ← TRUE
    END FOR
    IF NOT isCommon THEN
      sum ← sum + set1[i]
  END FOR

  // Loop for set2
  FOR i FROM 0 TO 4 DO
    isCommon ← FALSE
    FOR j FROM 0 TO 3 DO
      IF set2[i] = set1[j] THEN
        isCommon ← TRUE
    END FOR
    IF NOT isCommon THEN
      sum ← sum + set2[i]
  END FOR

  WRITE "Sum of distinct elements = ", sum
END


---

✅ Problem 2: Dot product + orthogonality check

pseudo
PROCEDURE dot_product(v1[10], v2[10], n: INTEGER, ps: OUT INTEGER)
VAR
  i ← INTEGER
BEGIN
  ps ← 0
  FOR i FROM 0 TO n - 1 DO
    ps ← ps + v1[i] * v2[i]
  END FOR
END


``pseudo
ALGORITHM check_orthogonality
VAR
  n ← INTEGER
  v1[10], v2[10] ← ARRAY OF INTEGER
  ps ← INTEGER
  i ← INTEGER

BEGIN
  READ n
  FOR i FROM 0 TO n - 1 DO
    READ v1[i], v2[i]
  END FOR

  CALL dot_product(v1, v2, n, ps)

  IF ps = 0 THEN
    WRITE "Vectors are orthogonal"
  ELSE
END
