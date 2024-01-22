## fayl sistemində SUID/GUID fayllarını axtarmaq üçün

#find / -perm -u=s -type f 2>/dev/nul

find - "tap" əmrini işə salır

/ - Bütün fayl sistemini axtarır

-perm - xüsusi icazələri olan faylları axtarır

-u=s - İstənilən icazə bit rejimi fayl üçün təyin edilmişdir. Bu formada simvolik rejimlər qəbul edilir

-tip f - Yalnız faylları axtarın

2>/dev/null - Səhvləri aradan qaldırır
