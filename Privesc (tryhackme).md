## fayl sistemində SUID/GUID fayllarını axtarmaq üçün

#find / -perm -u=s -type f 2>/dev/nul

1. find - "tap" əmrini işə salır

2. / - Bütün fayl sistemini axtarır

3. -perm - xüsusi icazələri olan faylları axtarır

4. -u=s - İstənilən icazə bit rejimi fayl üçün təyin edilmişdir. Bu formada simvolik rejimlər qəbul edilir

5. -tip f - Yalnız faylları axtarın

6. 2>/dev/null - Səhvləri aradan qaldırır
