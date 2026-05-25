+++
title = "Introduction to"
full_title = "Introduction to Differential Equations & Control with the Aerothrust Pendulum Part 2 PID Control"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/introduction-to-differential-equations-95a"
date = "2026-03-31"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/introduction-to-differential-equations-95a).

Introduction to Differential Equations & Control with the Aerothrust Pendulum : Part 2 - PID Control

# Introduction to Differential Equations & Control with the Aerothrust Pendulum : Part 2 - PID Control

### In this series of four articles, I explain the basics of differential equation and control theory (especially the mathematics behind it) by taking the simple example of an aerothrust pendulum

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Mar 31, 2026

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0iaWNvbiIgZmlsbD0iIzAwMDAwMCIgaGVpZ2h0PSIyMCIgcm9sZT0iaW1nIiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3R5bGU9ImhlaWdodDoyMHB4O3dpZHRoOjIwcHg7IiB2aWV3Ym94PSIwIDAgMjQgMjQiIHdpZHRoPSIyMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48Zz48dGl0bGU+PC90aXRsZT48c3ZnIGNsYXNzPSJsdWNpZGUgbHVjaWRlLWhlYXJ0IiBoZWlnaHQ9IjI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTE5IDE0YzEuNDktMS40NiAzLTMuMjEgMy01LjVBNS41IDUuNSAwIDAgMCAxNi41IDNjLTEuNzYgMC0zIC41LTQuNSAyLTEuNS0xLjUtMi43NC0yLTQuNS0yQTUuNSA1LjUgMCAwIDAgMiA4LjVjMCAyLjMgMS41IDQuMDUgMyA1LjVsNyA3WiIgLz48L3N2Zz4=)

3

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0iaWNvbiIgZmlsbD0iIzAwMDAwMCIgaGVpZ2h0PSIyMCIgcm9sZT0iaW1nIiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3R5bGU9ImhlaWdodDoyMHB4O3dpZHRoOjIwcHg7IiB2aWV3Ym94PSIwIDAgMjQgMjQiIHdpZHRoPSIyMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48Zz48dGl0bGU+PC90aXRsZT48c3ZnIGNsYXNzPSJsdWNpZGUgbHVjaWRlLW1lc3NhZ2UtY2lyY2xlIiBoZWlnaHQ9IjI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTcuOSAyMEE5IDkgMCAxIDAgNCAxNi4xTDIgMjJaIiAvPjwvc3ZnPg==)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0iaWNvbiIgZmlsbD0ibm9uZSIgaGVpZ2h0PSIyMCIgcm9sZT0iaW1nIiBzdHJva2U9InZhcigtLWNvbG9yLWZnLXByaW1hcnkpIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDIwIDIwIiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGc+PHRpdGxlPjwvdGl0bGU+PHBhdGggZD0iTTIuNTMwMDEgNy44MTU5NUMzLjQ5MTc5IDQuNzM5MTEgNi40MzI4MSAyLjUgOS45MTE3MyAyLjVDMTMuMTY4NCAyLjUgMTUuOTUzNyA0LjQ2MjE0IDE3LjA4NTIgNy4yMzY4NEwxNy42MTc5IDguNjc2NDdNMTcuNjE3OSA4LjY3NjQ3TDE4LjUwMDIgNC4yNjQ3MU0xNy42MTc5IDguNjc2NDdMMTMuNjQ3MyA2LjkxMTc2TTE3LjQ5OTUgMTIuMTg0MUMxNi41Mzc4IDE1LjI2MDkgMTMuNTk2NyAxNy41IDEwLjExNzggMTcuNUM2Ljg2MTE4IDE3LjUgNC4wNzU4OSAxNS41Mzc5IDIuOTQ0MzIgMTIuNzYzMkwyLjQxMTY1IDExLjMyMzVNMi40MTE2NSAxMS4zMjM1TDEuNTI5MyAxNS43MzUzTTIuNDExNjUgMTEuMzIzNUw2LjM4MjI0IDEzLjA4ODIiIC8+PC9nPjwvc3ZnPg==)

2

Share

Have you always been scared of differential equations? Did you feel so lost in your signals and systems or control systems class in your engineering and want to know what it actually meant? The following are the notes that I prepared as an undergraduate for conducing a workshop to teach control theory through a simple setup called the aerothrust pendulum. This is the second of a four part series of articles on differential equations, dynamical systems, and control theory. To read the first part, click here :

[](https://ramaseshanchandrasekaran.substack.com/p/introduction-to-differential-equations)

![Introduction to Differential Equations & Control with the Aerothrust Pendulum : Part 1 - Stability](https://substackcdn.com/image/fetch/$s_!17wE!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd010e99-265f-47cc-be29-c18e67dad757_618x452.heic)

#### Introduction to Differential Equations & Control with the Aerothrust Pendulum : Part 1 - Stability

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

Mar 30

[](https://ramaseshanchandrasekaran.substack.com/p/introduction-to-differential-equations)

Read full story![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1hcnJvdy1yaWdodCIgZmlsbD0ibm9uZSIgaGVpZ2h0PSIxNiIgc3Ryb2tlPSJjdXJyZW50Q29sb3IiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIyIiB2aWV3Ym94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNNSAxMmgxNCIgLz48cGF0aCBkPSJtMTIgNSA3IDctNyA3IiAvPjwvc3ZnPg==)

------------------------------------------------------------------------

Hi everyone, we meet again! Hope you were sane enough to get through the last article. Do not worry. You have crossed the tough part. Everything that follows now will be a consequence of what you have done so far. Once again we remind you of this aero thrust pendulum set up.

[](https://substackcdn.com/image/fetch/$s_!Iepw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66c7e8c3-8626-4b31-b88e-8cddea988a0e_742x442.heic)

![](https://substackcdn.com/image/fetch/$s_!Iepw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66c7e8c3-8626-4b31-b88e-8cddea988a0e_742x442.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

A brief review of what we have done before is given below. It is okay if you do not remember all the results. Just familiarize yourself again and again.

[](https://substackcdn.com/image/fetch/$s_!vhL3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc55374c7-4e38-4300-a63e-f22a800165b3_842x364.heic)

![](https://substackcdn.com/image/fetch/$s_!vhL3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc55374c7-4e38-4300-a63e-f22a800165b3_842x364.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!fuKv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdfef793f-ab43-4bba-99b0-30af1ec76b56_846x1174.heic)

![](https://substackcdn.com/image/fetch/$s_!fuKv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdfef793f-ab43-4bba-99b0-30af1ec76b56_846x1174.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!2CkK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5501d437-5c8c-48f7-8b5b-c7d06c27ca30_848x454.heic)

![](https://substackcdn.com/image/fetch/$s_!2CkK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5501d437-5c8c-48f7-8b5b-c7d06c27ca30_848x454.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

# A comment on Jacobian Linearization

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1saW5rIiBmaWxsPSJub25lIiBoZWlnaHQ9IjE4IiBzdHJva2U9ImN1cnJlbnRDb2xvciIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIHZpZXdib3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE4IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xMCAxM2E1IDUgMCAwIDAgNy41NC41NGwzLTNhNSA1IDAgMCAwLTcuMDctNy4wN2wtMS43MiAxLjcxIiAvPjxwYXRoIGQ9Ik0xNCAxMWE1IDUgMCAwIDAtNy41NC0uNTRsLTMgM2E1IDUgMCAwIDAgNy4wNyA3LjA3bDEuNzEtMS43MSIgLz48L3N2Zz4=)

Some of you might think that Jacobian linearization is only an approximation and hence is an inefficient and childish technique which we use only because we know how to solve linear differential equations easily. It is true that Jacobian linearization gives only local information about the solution. But a good controller should keep the system close to the set point and hence control design based on Jacobian linearization does work as long as the initial conditions are close enough to the set point and disturbances do not make it deviate too much into the non linear range. Also control systems are designed to be robust to modeling errors and disturbances. So, a good controller should make a system immune to the neglected non linearities and disturbances. If you are still skeptic, remember that next time you fly on an aircraft, you are safe and sound and also the fact that the control systems for aircraft is designed using Jacobian linearization about desired attitude! That should be enough proof that linear control does work. I am not saying that non linear control is not necessary. In fact for systems whose trajectories span a wide range of values, non linear control is required. What I say is one should not be skeptic about linear systems and linear control.

[](https://substackcdn.com/image/fetch/$s_!oRcn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff08ace84-1c26-4299-9819-39a18d4a562d_938x1328.heic)

![](https://substackcdn.com/image/fetch/$s_!oRcn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff08ace84-1c26-4299-9819-39a18d4a562d_938x1328.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

Now let us proceed further with control system design. The equation we have is

[](https://substackcdn.com/image/fetch/$s_!r3nm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34e12caf-2c6d-4c8b-909c-434b6b490946_362x54.heic)

![](https://substackcdn.com/image/fetch/$s_!r3nm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34e12caf-2c6d-4c8b-909c-434b6b490946_362x54.heic)

But let us first realize one thing. In the mass-spring-damper system, the force f(t) was the input. It could be directly controlled. But here the thrust T(t) cannot be directly produced or controlled. The original input is the voltage to the BLDC motor V(t) and this indirectly affects the thrust T(t).

[](https://substackcdn.com/image/fetch/$s_!os_U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6cfe68ff-a8f0-4d9f-99da-9aa53ee9a02c_864x176.heic)

![](https://substackcdn.com/image/fetch/$s_!os_U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6cfe68ff-a8f0-4d9f-99da-9aa53ee9a02c_864x176.heic)

We do not know the relationship between the voltage V(t) and the thrust T(t). It will also be a “differential equation” and when we “linearize” it, it will have the associated poles. But now we have two cascaded systems. But we make an approximation now that the poles for the first system are far into the left half plane and that the CF dies exceedingly fast. So that the relation between V(t) and T(t) is a static relation and not a differential equation. We assume that the relation between T(t) and V(t) is an ordinary static function like y=f(x), we have T=f(V), and not something dynamical like a spring block system. But how do we find this function f We now have

[](https://substackcdn.com/image/fetch/$s_!TYXa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29e6f879-bbd3-460c-b8d0-0a6b9c45519d_390x60.heic)

![](https://substackcdn.com/image/fetch/$s_!TYXa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29e6f879-bbd3-460c-b8d0-0a6b9c45519d_390x60.heic)

Apply a constant voltage V0 and allow a corresponding constant thrust f(V0) to be generated. We then wait and allow for 𝜃(𝑡) to reach a steady constant value (after transients have died) and so that the first and second derivatives of 𝜃(t) vanish . Now, at steady state,

[](https://substackcdn.com/image/fetch/$s_!PDW0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc12259ec-ab5c-4945-be7e-6c1d9a8d994a_284x50.heic)

![](https://substackcdn.com/image/fetch/$s_!PDW0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc12259ec-ab5c-4945-be7e-6c1d9a8d994a_284x50.heic)

or

[](https://substackcdn.com/image/fetch/$s_!nTZB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F23f66dc8-2e86-413d-b53d-ad1fcdb7b8df_362x78.heic)

![](https://substackcdn.com/image/fetch/$s_!nTZB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F23f66dc8-2e86-413d-b53d-ad1fcdb7b8df_362x78.heic)

[](https://substackcdn.com/image/fetch/$s_!FrKF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd073a4e4-8d80-4159-88a3-88ea1da3ed7d.heic)

![](https://substackcdn.com/image/fetch/$s_!FrKF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd073a4e4-8d80-4159-88a3-88ea1da3ed7d.heic)

The above four parameters can be measured experimentally and hence f(V) can be determined for different values of V by taking measurements for different values of 𝜃𝑆𝑆, which is done for different values of voltages V.

[](https://substackcdn.com/image/fetch/$s_!BE3O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F977c2d73-e0eb-4c29-b6ad-87eb4eb4e5d9_898x214.heic)

![](https://substackcdn.com/image/fetch/$s_!BE3O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F977c2d73-e0eb-4c29-b6ad-87eb4eb4e5d9_898x214.heic)

Now, using the above set points and a function plotter tool (even available in Ms Excel), we can get a best fit curve for f(V).

[](https://substackcdn.com/image/fetch/$s_!FQRE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ed0fd15-8222-44c7-89fc-c12c17688781_490x326.heic)

![](https://substackcdn.com/image/fetch/$s_!FQRE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ed0fd15-8222-44c7-89fc-c12c17688781_490x326.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

So we now have a look up table between thrust and voltage. We can design controllers as though T(t) is the input and we can look it up through this curve and generate the corresponding voltage V(t). Based on the sophistication, accuracy and range, a suitable order polynomial or cubic spline or any other suitable curve fitting technique can be used (For detailed account, refer the experimental report). So, we now have the relation between voltage and theta.

------------------------------------------------------------------------

# The Need for Feedback Control

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1saW5rIiBmaWxsPSJub25lIiBoZWlnaHQ9IjE4IiBzdHJva2U9ImN1cnJlbnRDb2xvciIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIHZpZXdib3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE4IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xMCAxM2E1IDUgMCAwIDAgNy41NC41NGwzLTNhNSA1IDAgMCAwLTcuMDctNy4wN2wtMS43MiAxLjcxIiAvPjxwYXRoIGQ9Ik0xNCAxMWE1IDUgMCAwIDAtNy41NC0uNTRsLTMgM2E1IDUgMCAwIDAgNy4wNyA3LjA3bDEuNzEtMS43MSIgLz48L3N2Zz4=)

Let us once again return to the mass-spring damper system for introduction to controllers and feedback systems. Once again consider the equation

[](https://substackcdn.com/image/fetch/$s_!8vXd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc856a0b3-c905-4d15-a27f-0e20c0bda360_276x60.heic)

![](https://substackcdn.com/image/fetch/$s_!8vXd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc856a0b3-c905-4d15-a27f-0e20c0bda360_276x60.heic)

let our task be that : With no input, x(t) should go to zero as quickly as possible. But the thing is that it always does not go to zero, the way we like, depending on the values of 𝑚, 𝑏, 𝑘. For a recap, the pictures are shown below.

[](https://substackcdn.com/image/fetch/$s_!qGBa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57bcaf32-9d8f-459d-932e-9af86e3ddd44_890x842.heic)

![](https://substackcdn.com/image/fetch/$s_!qGBa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57bcaf32-9d8f-459d-932e-9af86e3ddd44_890x842.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

Hope now you remember those curves. But, we do not want the system to go to zero in any of those arbitrarily colored fashions but we would like to go it in a specific manner. Of course what is that specific manner is one’s own taste and requirements.

“ Some people like it slow and smooth whereas some people like it fast and oscillating “

Anyways we would have a preference of where the poles should be depending upon our allowance of oscillations, reach time and settling time requirements. But I am the person who likes things be done the fastest but do not like oscillations. So I want the critically damped case. In other words, I would want 𝑏^2 = 4𝑚𝑘 𝑜𝑟 𝜉= 1. But the values of b,m,k we have for the spring-block system are god given and expecting us to purchase a new spring or damper or a mass is just too stupid to even think about.

Changing the hardware like the one mentioned above is impractical. Because the hardware is not built to satisfy pole requirements. It is built to satisfy several other requirements like power, efficiency, size etc.. Hardware that is built to satisfy pole requirements cannot always satisfy power or efficiency requirements. It is we, with our input scheme need to bring the given system into control. So, we now have an existing mass-spring-damper system with arbitrary poles satisfying

[](https://substackcdn.com/image/fetch/$s_!frLG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d2cb9e6-34b3-4813-adb0-f414a8d611bf.heic)

![](https://substackcdn.com/image/fetch/$s_!frLG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d2cb9e6-34b3-4813-adb0-f414a8d611bf.heic)

But we wish to have the closed loop poles somewhere else with some new value of ‘b’ and new value of ‘k’ satisfying 𝑏^2 = 4𝑚𝑘 (My desire is always the fastest response without oscillations). So the desired equation for the system would be

[](https://substackcdn.com/image/fetch/$s_!aAbq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d1d9796-44e9-47e8-87ae-0ad661386c1d.heic)

![](https://substackcdn.com/image/fetch/$s_!aAbq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d1d9796-44e9-47e8-87ae-0ad661386c1d.heic)

such that 𝑏′2 = 4𝑚𝑘′ and the characteristic equation 𝑚𝑠^2 + 𝑏′𝑠+ 𝑘′= 0 has roots in the desired place.

Let ∆𝑏 𝑎𝑛𝑑 ∆𝑘 be the additional damping term and spring term respectively needed to achieve the desired values b’ and k’ such that

[](https://substackcdn.com/image/fetch/$s_!hrFp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F237ba159-0387-44b5-a214-a4013f836a32.heic)

![](https://substackcdn.com/image/fetch/$s_!hrFp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F237ba159-0387-44b5-a214-a4013f836a32.heic)

If we could somehow bring those extra damping and spring terms, we can hope to achieve the desired response.

[](https://substackcdn.com/image/fetch/$s_!vaeN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff1af9a1-1f3d-4026-86a8-75e2e1e12d84_664x382.heic)

![](https://substackcdn.com/image/fetch/$s_!vaeN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff1af9a1-1f3d-4026-86a8-75e2e1e12d84_664x382.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

Or taking them to the other side,

[](https://substackcdn.com/image/fetch/$s_!ev3C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fea9807f4-95fa-4c9f-b990-1d9aacc5cd37_382x56.heic)

![](https://substackcdn.com/image/fetch/$s_!ev3C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fea9807f4-95fa-4c9f-b990-1d9aacc5cd37_382x56.heic)

But oh wait! We can do this! We can do this in the right hand side!! There was this long forgotten guy called 𝑢(𝑡) at the right hand side.

[](https://substackcdn.com/image/fetch/$s_!g293!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0ea90525-2076-4a64-847f-882a6c173c68_262x42.heic)

![](https://substackcdn.com/image/fetch/$s_!g293!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0ea90525-2076-4a64-847f-882a6c173c68_262x42.heic)

Let us now shun our narrow mind and expand our mind and allow for input force 𝑢 to not only depend on ‘t’ but also on ‘x’. After all ‘u’ is what the input force we apply. Whether we make it a function of ‘x’ or ‘t’ is our will. Let us now have

[](https://substackcdn.com/image/fetch/$s_!UWPI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F781230d5-7b9a-496f-8818-41768c9b1188.heic)

![](https://substackcdn.com/image/fetch/$s_!UWPI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F781230d5-7b9a-496f-8818-41768c9b1188.heic)

And choose ‘u’ such that

[](https://substackcdn.com/image/fetch/$s_!rRWw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F074352e1-2aae-4d84-9db2-2ccd471a1e4f.heic)

![](https://substackcdn.com/image/fetch/$s_!rRWw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F074352e1-2aae-4d84-9db2-2ccd471a1e4f.heic)

which is precisely the missing term we want! This solves our problem completely! This 𝑢=−∆𝒃 𝒙 −∆𝒌 𝒙 when substituted into the spring block equation, we get,

[](https://substackcdn.com/image/fetch/$s_!fi_Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F204a19a9-24d2-45d9-b3d4-0a1e0b08e600_718x156.heic)

![](https://substackcdn.com/image/fetch/$s_!fi_Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F204a19a9-24d2-45d9-b3d4-0a1e0b08e600_718x156.heic)

Which now gives the desired response!!

[](https://substackcdn.com/image/fetch/$s_!O58h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb37e89a0-876d-42e5-8303-5a5386267700_658x114.heic)

![](https://substackcdn.com/image/fetch/$s_!O58h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb37e89a0-876d-42e5-8303-5a5386267700_658x114.heic)

And this has the nice response that I want.

[](https://substackcdn.com/image/fetch/$s_!EQyF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F076db853-5968-48d6-8fb9-6495f690ddd3_896x418.heic)

![](https://substackcdn.com/image/fetch/$s_!EQyF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F076db853-5968-48d6-8fb9-6495f690ddd3_896x418.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

But we were able to do this magic only at a cost! What cost! The input ‘u’ is a function of the output ‘x’ too! So we have to measure ‘x’! In other words, we need to measure ‘x’ and feed the information back to decide the input ‘u’. Diagrammatically what we have done is shown below:

[](https://substackcdn.com/image/fetch/$s_!1kvW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38f4a326-e888-4586-8d91-9c625dad7032_892x866.heic)

![](https://substackcdn.com/image/fetch/$s_!1kvW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38f4a326-e888-4586-8d91-9c625dad7032_892x866.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

We have stumbled upon what is called as a “**FEEDACK LOOP**“ , this is our first encounter with the feedback loop! Hereafter, the entirety of control systems will only be feedback loops!

So, by measuring the output and making the input depend on output (or what people call commonly as “**closing the loop**!” in control theory), we can virtually bring in the effect of a spring and a damper. After all what is a spring doing? Depending on ‘x’, it applies a force proportional to it. You are doing the same with a sensor, computer and an actuator! Sensor measures ‘x’, computer computes the force and actuator applies the corresponding force to the system! Similarly for thedamper! You are virtually realizing springs and dampers without actually purchasing them! So, this is what again I say is called “**feedback control**”.

> **Please remember that it is only through feedback that we can change
> the CF which otherwise cannot be changed if the input is only a
> function of time and is “blind” to what is actually happening at the
> output side!**

[](https://substackcdn.com/image/fetch/$s_!6Hij!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8abe877-544b-4215-ba43-48451291ec1d_1024x782.heic)

![](https://substackcdn.com/image/fetch/$s_!6Hij!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8abe877-544b-4215-ba43-48451291ec1d_1024x782.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!qi-j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99fb584f-de0d-483a-ba4a-6fed6d451a93_698x416.heic)

![](https://substackcdn.com/image/fetch/$s_!qi-j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99fb584f-de0d-483a-ba4a-6fed6d451a93_698x416.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

------------------------------------------------------------------------

# The PID Controller

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1saW5rIiBmaWxsPSJub25lIiBoZWlnaHQ9IjE4IiBzdHJva2U9ImN1cnJlbnRDb2xvciIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIHZpZXdib3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE4IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xMCAxM2E1IDUgMCAwIDAgNy41NC41NGwzLTNhNSA1IDAgMCAwLTcuMDctNy4wN2wtMS43MiAxLjcxIiAvPjxwYXRoIGQ9Ik0xNCAxMWE1IDUgMCAwIDAtNy41NC0uNTRsLTMgM2E1IDUgMCAwIDAgNy4wNyA3LjA3bDEuNzEtMS43MSIgLz48L3N2Zz4=)

The above feedback control law which we discussed just now given by

[](https://substackcdn.com/image/fetch/$s_!YEz5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14da2acb-66c6-42dc-afb7-eb682664fb65.heic)

![](https://substackcdn.com/image/fetch/$s_!YEz5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14da2acb-66c6-42dc-afb7-eb682664fb65.heic)

is called the “PD controller”.

‘P’ stands for proportional.

‘D’ stands for derivative.

Here, the desired or the reference point for the output ‘x’ is zero.

[](https://substackcdn.com/image/fetch/$s_!o2lB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F919c3051-d76a-4cfe-b190-3e49d7e39f2d_676x42.heic)

![](https://substackcdn.com/image/fetch/$s_!o2lB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F919c3051-d76a-4cfe-b190-3e49d7e39f2d_676x42.heic)

So the control law can also be written as

[](https://substackcdn.com/image/fetch/$s_!CDA1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25a412ca-9fec-4423-88b4-e59255c5ddd5_552x318.heic)

![](https://substackcdn.com/image/fetch/$s_!CDA1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25a412ca-9fec-4423-88b4-e59255c5ddd5_552x318.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

So, this controller is a special case of the generic structure of a class of controllers called **PD controller** where the input has sum of terms proportional to the error and its derivative. This is the most widely used controller in industry (just one more term for that) and is inspired from the spring block system.

The proportional term is like a virtual spring, whose reference or equilibrium is the set point and hence it applies input to bring the error to zero or the output to the set point.

The derivative term is like a virtual damper which tries to dampen the oscillations and induce stability into the system by opposing and hence preventing fast changes in the output.

So, this is the philosophy behind the popularly used PD controller. Now, can we apply this PD controller to the aero thrust pendulum? We have the following model.

[](https://substackcdn.com/image/fetch/$s_!e2uX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b22fb56-7186-4591-a84e-5e700f80d9f4_390x60.heic)

![](https://substackcdn.com/image/fetch/$s_!e2uX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b22fb56-7186-4591-a84e-5e700f80d9f4_390x60.heic)

Note that we can treat T(t) as the input since it has a static look-up table kind of relationship with the actual input which is voltage V(t). Therefore one can design for T(t) and then use the look up table to generate V(t). If our desired angle were zero degrees, then we could use the small angle approximation for the sine function and we would have

[](https://substackcdn.com/image/fetch/$s_!OWqn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff904c92a-5582-404f-8200-93bce6f718ff_354x52.heic)

![](https://substackcdn.com/image/fetch/$s_!OWqn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff904c92a-5582-404f-8200-93bce6f718ff_354x52.heic)

Therefore, the controller is

[](https://substackcdn.com/image/fetch/$s_!ykZe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98680285-b2c1-43ad-accf-beafebc05865_604x250.heic)

![](https://substackcdn.com/image/fetch/$s_!ykZe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98680285-b2c1-43ad-accf-beafebc05865_604x250.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!aU6n!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0233394f-95fd-40ef-88b7-4a8b87423c70_514x58.heic)

![](https://substackcdn.com/image/fetch/$s_!aU6n!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0233394f-95fd-40ef-88b7-4a8b87423c70_514x58.heic)

But again, this controller will work only for set point of zero degrees. (We have linearized or straightened the curve around zero degrees). What should we do if the set point is some other arbitrary value?

[](https://substackcdn.com/image/fetch/$s_!YTc4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0938a9bb-89e6-49b2-ba61-a1d4111ac10e_902x1002.heic)

![](https://substackcdn.com/image/fetch/$s_!YTc4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0938a9bb-89e6-49b2-ba61-a1d4111ac10e_902x1002.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!YC3k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb503c45-7a86-4ced-a2ce-d9f8437c409a_884x408.heic)

![](https://substackcdn.com/image/fetch/$s_!YC3k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb503c45-7a86-4ced-a2ce-d9f8437c409a_884x408.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

But there is again one annoying term sitting there!

[](https://substackcdn.com/image/fetch/$s_!OVOT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f1cea7d-cd38-46ee-aa08-b03e9494e285_736x226.heic)

![](https://substackcdn.com/image/fetch/$s_!OVOT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f1cea7d-cd38-46ee-aa08-b03e9494e285_736x226.heic)

This term destroys homogeneity! (Check that for yourself in exercises) . Still system is non linear since it does not satisfy homogeneity!

[](https://substackcdn.com/image/fetch/$s_!Q763!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d69d0f0-0632-4876-9669-9864b2220f47_728x314.heic)

![](https://substackcdn.com/image/fetch/$s_!Q763!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d69d0f0-0632-4876-9669-9864b2220f47_728x314.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

But you are right! We can destroy terms with the input as we could add new spring or damper terms previously. Taking to the right hand side,

[](https://substackcdn.com/image/fetch/$s_!zbzJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a92a2e5-f7ea-4bea-95ac-92e29338aff9_756x108.heic)

![](https://substackcdn.com/image/fetch/$s_!zbzJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a92a2e5-f7ea-4bea-95ac-92e29338aff9_756x108.heic)

where u is now split into two parts. One part is responsible for cancelling

[](https://substackcdn.com/image/fetch/$s_!EVba!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F70d5f92f-b646-4169-a2f6-50d150277fce.heic)

![](https://substackcdn.com/image/fetch/$s_!EVba!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F70d5f92f-b646-4169-a2f6-50d150277fce.heic)

after which we have the system

[](https://substackcdn.com/image/fetch/$s_!TuNs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe67dfd01-6c02-41de-ac3b-3637debd6003_408x52.heic)

![](https://substackcdn.com/image/fetch/$s_!TuNs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe67dfd01-6c02-41de-ac3b-3637debd6003_408x52.heic)

Now, choose ‘w’, the remaining input as a feedback of e and de/dt and now, which is

[](https://substackcdn.com/image/fetch/$s_!_ax5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba129a09-6c91-4588-9339-ba50c3ea8edd.heic)

![](https://substackcdn.com/image/fetch/$s_!_ax5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba129a09-6c91-4588-9339-ba50c3ea8edd.heic)

which then leads to

[](https://substackcdn.com/image/fetch/$s_!9yf-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F475d7438-8300-434f-aae5-c98cdc1496e3_526x60.heic)

![](https://substackcdn.com/image/fetch/$s_!9yf-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F475d7438-8300-434f-aae5-c98cdc1496e3_526x60.heic)

The characteristic equation is

[](https://substackcdn.com/image/fetch/$s_!cd5d!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e40a784-135a-48f3-a305-e28fbef6de84_500x46.heic)

![](https://substackcdn.com/image/fetch/$s_!cd5d!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e40a784-135a-48f3-a305-e28fbef6de84_500x46.heic)

Now, Kp and Kd can be tuned to place the roots of the characteristic equation in the desired place. For example,

[](https://substackcdn.com/image/fetch/$s_!0EKq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe7767ba-efff-400b-a174-0ed1bd4504f7_738x166.heic)

![](https://substackcdn.com/image/fetch/$s_!0EKq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe7767ba-efff-400b-a174-0ed1bd4504f7_738x166.heic)

Thus, this is how we control the aero thrust pendulum about any arbitrary set point using Jacobian linearization. Yes, it is the fact that the Jacobian linearization is valid only in the local range around the set point but under high gain feedback, it works so well in wide ranges (since the non linearities can be neglected under high gain feedback). Let us do an analysis.

[](https://substackcdn.com/image/fetch/$s_!Q7y8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F334090e9-1b85-4aba-89d2-fc32efe23b3b_898x78.heic)

![](https://substackcdn.com/image/fetch/$s_!Q7y8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F334090e9-1b85-4aba-89d2-fc32efe23b3b_898x78.heic)

Here is to those skeptics who pondered about the physical meaning of a negative spring constant!! The characteristic equation without w(t) is

[](https://substackcdn.com/image/fetch/$s_!e9Yj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38aab989-ccc6-4f45-aa71-3a9ef45a9fd3_378x78.heic)

![](https://substackcdn.com/image/fetch/$s_!e9Yj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38aab989-ccc6-4f45-aa71-3a9ef45a9fd3_378x78.heic)

[](https://substackcdn.com/image/fetch/$s_!Katq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b5a2e57-0c24-4d56-9600-dd57724e946d_298x48.heic)

![](https://substackcdn.com/image/fetch/$s_!Katq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b5a2e57-0c24-4d56-9600-dd57724e946d_298x48.heic)

definitely at least one of the roots is in the right half plane. Which is why using just the input

[](https://substackcdn.com/image/fetch/$s_!94Be!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6872d319-306e-4fba-bfa5-67bdb8d73094.heic)

![](https://substackcdn.com/image/fetch/$s_!94Be!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6872d319-306e-4fba-bfa5-67bdb8d73094.heic)

(that cancels gravity at set point), it is impossible to keep the pendulum around 𝜃𝑅 without using any additional feedback input w(t).

[](https://substackcdn.com/image/fetch/$s_!tcux!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb01fbb3e-7c80-4335-b0bb-b5c0337ea9fd_438x46.heic)

![](https://substackcdn.com/image/fetch/$s_!tcux!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb01fbb3e-7c80-4335-b0bb-b5c0337ea9fd_438x46.heic)

the spring constant becomes smaller and smaller or the strength of the spring decreases. So, the transient performance deteriorates and we observe more overshoots or excessive settling times.

[](https://substackcdn.com/image/fetch/$s_!RCok!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5a68354-0e78-4f99-80f0-a6625ae1c8aa_408x54.heic)

![](https://substackcdn.com/image/fetch/$s_!RCok!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5a68354-0e78-4f99-80f0-a6625ae1c8aa_408x54.heic)

and hence there is no need for gravity cancellation at the vertically up position. But, we all know intuitively that if we make a rod stand upright vertical without any input, it will fall down. Now we know it mathematically too because the CF (zero input solution) is unstable as the spring constant is negative around vertically up position and hence even small non zero initial condition will make it falling. Now, let us return to the spring block system! Let us see if PD control is sufficient for all purposes.

[](https://substackcdn.com/image/fetch/$s_!VXpx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9b09511-3413-413c-aac7-b3c863b3714e_288x94.heic)

![](https://substackcdn.com/image/fetch/$s_!VXpx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9b09511-3413-413c-aac7-b3c863b3714e_288x94.heic)

------------------------------------------------------------------------

# Constant Disturbances, Need for Integral Action & PID Control

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1saW5rIiBmaWxsPSJub25lIiBoZWlnaHQ9IjE4IiBzdHJva2U9ImN1cnJlbnRDb2xvciIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIHZpZXdib3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE4IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xMCAxM2E1IDUgMCAwIDAgNy41NC41NGwzLTNhNSA1IDAgMCAwLTcuMDctNy4wN2wtMS43MiAxLjcxIiAvPjxwYXRoIGQ9Ik0xNCAxMWE1IDUgMCAwIDAtNy41NC0uNTRsLTMgM2E1IDUgMCAwIDAgNy4wNyA3LjA3bDEuNzEtMS43MSIgLz48L3N2Zz4=)

Let us consider PD control but now let us assume two scenarios:

(i)An unknown but constant disturbance ‘d’ is acting on the system along with the control input.

\(ii\) x=0 is no longer the reference point for me. I want to go to x=r !

So now we need to modify the PD control law as

[](https://substackcdn.com/image/fetch/$s_!WxEx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d1c75b0-29b8-45c3-96ca-607cb738032c_488x56.heic)

![](https://substackcdn.com/image/fetch/$s_!WxEx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d1c75b0-29b8-45c3-96ca-607cb738032c_488x56.heic)

(We need to create a virtual spring now centered at ‘r’ instead of ‘x=0’)

(’d’ is the constant disturbance)

So, in closed loop, it becomes

[](https://substackcdn.com/image/fetch/$s_!tjbG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a96df31-2e92-42c8-8420-4483cb0161d7_482x44.heic)

![](https://substackcdn.com/image/fetch/$s_!tjbG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a96df31-2e92-42c8-8420-4483cb0161d7_482x44.heic)

[](https://substackcdn.com/image/fetch/$s_!9q4U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ab42ffc-35e9-46a2-b6c0-0e1ef5f57464_920x648.heic)

![](https://substackcdn.com/image/fetch/$s_!9q4U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ab42ffc-35e9-46a2-b6c0-0e1ef5f57464_920x648.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

But high gain is not desirable for several reasons. First, the frequency of oscillations will increase, and it may also lead to instability of the CF for higher order systems (even a second order system may have fast higher order modes which we may have neglected). Also high gain leads to control saturation and chattering and is an open invitation for noise to affect the system.

[](https://substackcdn.com/image/fetch/$s_!jS2u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F017b3cf9-ea64-4022-849c-bb9be3f56823_382x112.heic)

![](https://substackcdn.com/image/fetch/$s_!jS2u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F017b3cf9-ea64-4022-849c-bb9be3f56823_382x112.heic)

Even in the case of zero reference, reference is achieved only in presence of no constant disturbances. But constant disturbances are so common to systems and slowly varying disturbances are also common which can be approximated as constants. In the case of an aero thrust pendulum, one source of the constant disturbance happens when we use this equation

[](https://substackcdn.com/image/fetch/$s_!EfBo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3462704-d673-418c-bd99-533f2dd59a4b_276x40.heic)

![](https://substackcdn.com/image/fetch/$s_!EfBo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3462704-d673-418c-bd99-533f2dd59a4b_276x40.heic)

We may not know the value of 𝑚𝑔 𝑙𝐶𝑀 perfectly or some additional load may be added to the system which when happens, becomes

[](https://substackcdn.com/image/fetch/$s_!2Bsz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19a8d40e-fa5c-441b-bc34-0a58a33dfae7_906x864.heic)

![](https://substackcdn.com/image/fetch/$s_!2Bsz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19a8d40e-fa5c-441b-bc34-0a58a33dfae7_906x864.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

So we need robustness to this type of disturbance. One strategy which would have entered your nerves by now is to cancel the disturbance using the control input. But we do not know the error to cancel it in the first place. Again, let us illustrate this situation through a comic as shown in the next page. So we need control systems that are robust to these constant disturbances.

But in spite of any reasonable value of 𝐾𝑃 & 𝐾𝐷, the error does not go to zero. So, we now state a statement universal in all textbooks.

> **“Use of a PD controller results in steady state error”**

We need another scheme to be integrated with PD to eliminate steady state error. Who thought this would literally be an integration! Basically, let us examine the root cause of this steady state error. Consider once again the spring block system.

[](https://substackcdn.com/image/fetch/$s_!pv_q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdbd1c1f-bd59-4a7f-a51e-6821b0ef3727_466x52.heic)

![](https://substackcdn.com/image/fetch/$s_!pv_q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdbd1c1f-bd59-4a7f-a51e-6821b0ef3727_466x52.heic)

The system now has two springs! A real spring “ 𝑘𝑥” which wants to make 𝑥→0 and a virtual spring 𝐾p(𝑥−𝑟) which wants to make 𝑥→𝑟. And a disturbance ‘d’ which wants to make it go somewhere else. At steady state, system settles to a state where the pull from all these three effects cancel. As 𝐾𝑃 →∞, the pull of the virtual spring is stronger as the virtual spring constant is increased and hence system moves closer to ‘r’ at steady state as 𝐾𝑃 →∞. Now, how do we design a controller that is robust under unknown but constant disturbances? We want the steady state error to go to zero at any cost except high gain. Let us think. The controller we have designed was intelligent enough so that it creates a spring effect to create the tendency of the system to go to ‘r’ and also a damping effect to prevent rapid changes or oscillations. But it is not intelligent enough to fight against the constant disturbance that makes it go a little bit off. We are told not to use our strength (high gain) to win this war. So we should use intelligence. We feed control inputs proportional to error only. It sees only the error at present. But under disturbance, there is a steady state error that is persistent even after transients die. The proportional scheme has no way of detecting that this steady state error is there for a long time. Whether the error is present 3 seconds after t=0 or 3 years after the system is ON, the proportional controller will give the same response. Now I hope you get the problem. When the error is persistent for a long time (steady state), we have to apply a larger input. So the time of error or accumulated error should also be used to fight against the disturbance. Now, integration of error is a measure of accumulation of error.

[](https://substackcdn.com/image/fetch/$s_!21k3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F625551aa-c038-4224-a7e9-d366d82f7803_1010x1248.heic)

![](https://substackcdn.com/image/fetch/$s_!21k3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F625551aa-c038-4224-a7e9-d366d82f7803_1010x1248.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

So, we now propose

[](https://substackcdn.com/image/fetch/$s_!pMPM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c94b15f-1cd2-41b1-85ab-a4fe262d849f_628x120.heic)

![](https://substackcdn.com/image/fetch/$s_!pMPM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c94b15f-1cd2-41b1-85ab-a4fe262d849f_628x120.heic)

Now, the system uses the integral action to fight against the system spring and the constant disturbance. It no longer applies the same input under steady state error but pushes harder when it is staying with the same steady state error for a long time. So, in closed loop, the system becomes

[](https://substackcdn.com/image/fetch/$s_!3clR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F291f990e-9f32-4ab3-b655-80d024e8022b_644x128.heic)

![](https://substackcdn.com/image/fetch/$s_!3clR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F291f990e-9f32-4ab3-b655-80d024e8022b_644x128.heic)

But we now have an integration term in the differential equation. This is now an integro-differential equation! A new beast! But enough of this. Differential equations itself was enough trouble.

[](https://substackcdn.com/image/fetch/$s_!Lf9F!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa360e42e-2fd4-49b1-9a01-bd3a0ab99797_634x128.heic)

![](https://substackcdn.com/image/fetch/$s_!Lf9F!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa360e42e-2fd4-49b1-9a01-bd3a0ab99797_634x128.heic)

Differentiate both sides so that we undo the integration, and whoa! We get back our old friend or beast, the differential equation!

[](https://substackcdn.com/image/fetch/$s_!mgmi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F31e18871-241e-4fb0-a71c-77837c78eb77_706x168.heic)

![](https://substackcdn.com/image/fetch/$s_!mgmi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F31e18871-241e-4fb0-a71c-77837c78eb77_706x168.heic)

But notice that now this is a third order differential equation.

[](https://substackcdn.com/image/fetch/$s_!wlXl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9e4a729d-ed3e-430f-97ab-0155ca00aabf_514x164.heic)

![](https://substackcdn.com/image/fetch/$s_!wlXl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9e4a729d-ed3e-430f-97ab-0155ca00aabf_514x164.heic)

[](https://substackcdn.com/image/fetch/$s_!9UsV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e8445ef-a1e6-4ad3-8bb5-2fe81b065782_660x320.heic)

![](https://substackcdn.com/image/fetch/$s_!9UsV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e8445ef-a1e6-4ad3-8bb5-2fe81b065782_660x320.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

Note that we do not have the disturbance term in this equation! The behavior of error is independent of the disturbance! This is a third order linear differential equation with no input and hence the solution is the CF given by three poles as

[](https://substackcdn.com/image/fetch/$s_!Zfzq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4887d8b3-9949-42a3-859e-8d46019ca8cf_694x164.heic)

![](https://substackcdn.com/image/fetch/$s_!Zfzq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4887d8b3-9949-42a3-859e-8d46019ca8cf_694x164.heic)

But we have a problem now. We cannot guarantee that 𝑒(𝑡) →0 since we do not know that all three roots s1,s2,s3 are in the left half plane for all values of KI. In the second order case,

[](https://substackcdn.com/image/fetch/$s_!lgMM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fab2b76b7-283d-4242-98b3-08ff7ad9829d.heic)

![](https://substackcdn.com/image/fetch/$s_!lgMM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fab2b76b7-283d-4242-98b3-08ff7ad9829d.heic)

we were guaranteed that both the roots are in the left half plane as long as 𝑚, 𝑏, 𝑘\> 0. But there is no assurance like that for third order systems even if

[](https://substackcdn.com/image/fetch/$s_!8eaD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20bb0e29-0ac6-476d-9559-7c135efec1a8_340x54.heic)

![](https://substackcdn.com/image/fetch/$s_!8eaD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20bb0e29-0ac6-476d-9559-7c135efec1a8_340x54.heic)

------------------------------------------------------------------------

# Root Locus

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1saW5rIiBmaWxsPSJub25lIiBoZWlnaHQ9IjE4IiBzdHJva2U9ImN1cnJlbnRDb2xvciIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIHZpZXdib3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE4IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xMCAxM2E1IDUgMCAwIDAgNy41NC41NGwzLTNhNSA1IDAgMCAwLTcuMDctNy4wN2wtMS43MiAxLjcxIiAvPjxwYXRoIGQ9Ik0xNCAxMWE1IDUgMCAwIDAtNy41NC0uNTRsLTMgM2E1IDUgMCAwIDAgNy4wNyA3LjA3bDEuNzEtMS43MSIgLz48L3N2Zz4=)

Then how do the roots behave as KI is varied? So we need to be careful in case of controller design for higher order systems. We cannot set randomly the value of KI. How do we study the evolution of roots for a third order system as one of its coefficients of its characteristic equation varies?

So you see how algebra is hooking up with dynamics. Let us start with the simple case. Consider a first order characteristic equation

[](https://substackcdn.com/image/fetch/$s_!6FC7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ad96414-9f09-4b46-b01b-54f037f1a03f.heic)

![](https://substackcdn.com/image/fetch/$s_!6FC7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ad96414-9f09-4b46-b01b-54f037f1a03f.heic)

Consider this as a result of applying integral action for a zero order system (with no damper and mass, just the spring). We see that

[](https://substackcdn.com/image/fetch/$s_!GR71!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18a81f8b-b7bb-4a62-ab5b-31f6039d0598.heic)

![](https://substackcdn.com/image/fetch/$s_!GR71!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18a81f8b-b7bb-4a62-ab5b-31f6039d0598.heic)

and hence the single root of the characteristic equation starts from zero and keeps moving along the negative direction of the real axis, becoming more negative. A simple sketch of what is called the “**ROOT LOCUS”** is shown for the first order system.

[](https://substackcdn.com/image/fetch/$s_!ui31!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d84c88b-14e7-4c0d-a4ba-8d0d9a41f31c_866x410.heic)

![](https://substackcdn.com/image/fetch/$s_!ui31!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d84c88b-14e7-4c0d-a4ba-8d0d9a41f31c_866x410.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

So a first order system behavior is simple in structure under variation of the constant term in the characteristic equation. Let us now come to the second order case.

[](https://substackcdn.com/image/fetch/$s_!4Y92!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd6fb0f4-9208-4198-ad7f-6e0ec9c752d9.heic)

![](https://substackcdn.com/image/fetch/$s_!4Y92!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd6fb0f4-9208-4198-ad7f-6e0ec9c752d9.heic)

We already know that if a, KI\> 0, then all roots are in the left half plane. But how will they travel? When KI=0, then the poles are at

[](https://substackcdn.com/image/fetch/$s_!LTZc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0592b534-8f0d-4d8a-b0c3-ac1dfaec69bf.heic)

![](https://substackcdn.com/image/fetch/$s_!LTZc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0592b534-8f0d-4d8a-b0c3-ac1dfaec69bf.heic)

Then, we have

[](https://substackcdn.com/image/fetch/$s_!efyd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F88203121-b222-450d-99d9-53570ab5052b_874x874.heic)

![](https://substackcdn.com/image/fetch/$s_!efyd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F88203121-b222-450d-99d9-53570ab5052b_874x874.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!Qug0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75cb11d0-2076-4f49-aa33-a58a6b9ccd30_824x482.heic)

![](https://substackcdn.com/image/fetch/$s_!Qug0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75cb11d0-2076-4f49-aa33-a58a6b9ccd30_824x482.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

I hope you now appreciate the idea of a “root locus” diagram. It is much more informative than the equations. A picture is worth a thousand words. We see that the roots initially being highly over damped, as the gain increases, come closer and closer and become equal (critically damped) at the breakaway point and then after that enter into the complex plane with the real part being same as the breakaway point and the imaginary part increasing with gain. But as already commented, as long as m,b,KI\>0, the roots never enter the right half plane. But what about the third order equation

[](https://substackcdn.com/image/fetch/$s_!yirp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff628d06f-9f36-403d-a494-4a5ddd7b0e03_308x56.heic)

![](https://substackcdn.com/image/fetch/$s_!yirp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff628d06f-9f36-403d-a494-4a5ddd7b0e03_308x56.heic)

Do any of you know the formulae for the roots of the cubic equation? The sad news is there is not an easy one. So does that spell the doom for sketching the root locus? But all hope is not lost. We can have a feel of the root locus even if we don’t know the exact formulae of the root locus. First let us take the case of KI=0. Then the characteristic equation becomes

[](https://substackcdn.com/image/fetch/$s_!kK32!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5aa6a32a-5ac2-4be4-b26d-abb93cdbf9af_806x366.heic)

![](https://substackcdn.com/image/fetch/$s_!kK32!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5aa6a32a-5ac2-4be4-b26d-abb93cdbf9af_806x366.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

Let us now ask where do the roots go to as the integral gain very high. ie. where do the roots tend to as 𝐾𝐼 →∞. When the gain becomes high, we have two cases:

**(i) A root tends to a finite limit**

The equation is

[](https://substackcdn.com/image/fetch/$s_!VZx_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61fd0fbe-fcfe-408f-ac72-7a4dd68522ed_292x34.heic)

![](https://substackcdn.com/image/fetch/$s_!VZx_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61fd0fbe-fcfe-408f-ac72-7a4dd68522ed_292x34.heic)

If the root ‘s’ satisfying the above equation goes to a finite limit as 𝐾𝐼 →∞, then the finite stuff can be neglected compared to a large number and hence we have 𝐾𝐼 = 0 . But this is impossible. Thus, under the variation of only the constant term, the roots of a polynomial equation can never go to a finite limit.

**(ii) The root goes out of bound**

The other case is the root also goes to infinity, divergent in the complex plane. Now, as 𝐾𝐼 →∞, 𝑎𝑙𝑠𝑜 𝑠→∞. We have

[](https://substackcdn.com/image/fetch/$s_!MrOI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9211aeb6-ff0a-4878-89f6-8453b7aa4720_292x44.heic)

![](https://substackcdn.com/image/fetch/$s_!MrOI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9211aeb6-ff0a-4878-89f6-8453b7aa4720_292x44.heic)

So, as s→∞, only the higher powers of ‘s’ will dominate. Thus, it is enough if we take the cubes and squares only. You might ask why not just retain the cubes, but it turns out that it gives very crude approximation to the root locus. So, we retain only the first two leading powers and we have

[](https://substackcdn.com/image/fetch/$s_!NykA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61da2d0c-aee7-496c-83b3-7dba84c15f83_574x106.heic)

![](https://substackcdn.com/image/fetch/$s_!NykA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61da2d0c-aee7-496c-83b3-7dba84c15f83_574x106.heic)

[](https://substackcdn.com/image/fetch/$s_!1Qpi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f6d85bc-b798-4516-bb5e-3309ea8e6fc1_896x1192.heic)

![](https://substackcdn.com/image/fetch/$s_!1Qpi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f6d85bc-b798-4516-bb5e-3309ea8e6fc1_896x1192.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!25AK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdf191265-fd4a-4c84-a0ab-ce0356bbe2cb_878x1110.heic)

![](https://substackcdn.com/image/fetch/$s_!25AK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdf191265-fd4a-4c84-a0ab-ce0356bbe2cb_878x1110.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!w5Xz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F496e1925-5d26-49ab-a5d8-467c649c8ee3_888x1280.heic)

![](https://substackcdn.com/image/fetch/$s_!w5Xz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F496e1925-5d26-49ab-a5d8-467c649c8ee3_888x1280.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!_-UU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c488b6b-60e4-47e4-b076-0afafe7c48bb_1040x748.heic)

![](https://substackcdn.com/image/fetch/$s_!_-UU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c488b6b-60e4-47e4-b076-0afafe7c48bb_1040x748.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

But in between what does the root locus do? How does it approach the asymptotes? What does it do when the roots are real? Let us now examine what parts of the real axis does the root locus penetrate into since the roots are real for small gains.

[](https://substackcdn.com/image/fetch/$s_!t4Xy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe97cb52-3143-4687-976d-5ed4fa77d870_608x178.heic)

![](https://substackcdn.com/image/fetch/$s_!t4Xy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe97cb52-3143-4687-976d-5ed4fa77d870_608x178.heic)

[](https://substackcdn.com/image/fetch/$s_!Mm8s!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc35c47f0-4016-420e-aff6-a5e2cbb3bd24_882x1188.heic)

![](https://substackcdn.com/image/fetch/$s_!Mm8s!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc35c47f0-4016-420e-aff6-a5e2cbb3bd24_882x1188.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

[](https://substackcdn.com/image/fetch/$s_!mYry!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8fd75d6-6b86-4aaa-bc6f-fdc909181554_1040x958.heic)

![](https://substackcdn.com/image/fetch/$s_!mYry!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8fd75d6-6b86-4aaa-bc6f-fdc909181554_1040x958.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

The root locus initially begins at the open loop poles s1,s2,s3 and one of the branches at the left always remains real and goes farther left as gain increases. (This root is well behaved as far as stability is concerned and in a cubic equation one root always has to be real). The next two branches now approach each other (no other go as if it were not, then they would have to exist in the forbidden region of the real axis) . They now should collide at some breakaway point (as it did in the second order case) and then make an entry into the imaginary axis. But as gain further increases, the root locus (which remained stable in the second order case) now branches off and crosses the imaginary axis at some critical gain and then marches into the right half plane where it gradually converges to the asymptotes. The real root locus sketch for a third order system as shown in Matlab is shown below for

[](https://substackcdn.com/image/fetch/$s_!4MH5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F401409e4-bcc7-4fee-91e4-de6631ed988b_868x762.heic)

![](https://substackcdn.com/image/fetch/$s_!4MH5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F401409e4-bcc7-4fee-91e4-de6631ed988b_868x762.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

We find that the critical gain for this system is about 11. So, we see that the we can trace the evolution of roots of the characteristic equation roughly as any parameter of an algebraic equation is varied by looking at the open loop roots, finite and infinite asymptotes and the real axis traces. We can use similar arguments like below. We can also find exactly the critical gain and the frequency of oscillation at the critical gain using a technique called the **Routh-Hurwitz criterion.** For the procedure to be followed, refer any standard text on control theory. Also there is a procedure to find exactly the breakaway points which is present on any standard text on control theory. Also if the open loop poles are complex conjugate, there are also techniques to find the angle of departure of root locus from the open loop pole. Such quantitative details while greatly refining the sketch of the root locus can nowadays be performed by a computer. But a computer cannot substitute a good understanding of the qualitative features of a root locus. In the exercises, you will attempt to sketch the root loci for many other systems.

So, we have to fix KP, KD, KI such that the root locus crosses the desired poles we want. The techniques followed in the above example lead to generic rules for doing the qualitative sketch of the root locus for any arbitrary system with any arbitrary varying parameter in the characteristic equation that can be found in all textbooks. See the experimental record that demonstrates the effect of varying integral gains for the aero thrust pendulum where the instability of the aero thrust pendulum under high values of gain is demonstrated. In the aero pendulum, again the above analogy carries forward.

[](https://substackcdn.com/image/fetch/$s_!lIO5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7ad9c3b9-285d-4659-b86c-d74f43f609e2_248x170.heic)

![](https://substackcdn.com/image/fetch/$s_!lIO5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7ad9c3b9-285d-4659-b86c-d74f43f609e2_248x170.heic)

------------------------------------------------------------------------

# Trajectory control : Feed-Forward + Feedback

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1saW5rIiBmaWxsPSJub25lIiBoZWlnaHQ9IjE4IiBzdHJva2U9ImN1cnJlbnRDb2xvciIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIHZpZXdib3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE4IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xMCAxM2E1IDUgMCAwIDAgNy41NC41NGwzLTNhNSA1IDAgMCAwLTcuMDctNy4wN2wtMS43MiAxLjcxIiAvPjxwYXRoIGQ9Ik0xNCAxMWE1IDUgMCAwIDAtNy41NC0uNTRsLTMgM2E1IDUgMCAwIDAgNy4wNyA3LjA3bDEuNzEtMS43MSIgLz48L3N2Zz4=)

So far we dealt with set point control where the desired value of output is a constant. Now let us deal with trajectory tracking where we want the output to not reach a particular level and settle, but follow a time varying trajectory. Again consider the spring block system. So consider now a generic desired trajectory

[](https://substackcdn.com/image/fetch/$s_!unjk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f7f52ef-c25d-4b93-b912-92b272b4e0b6_794x588.heic)

![](https://substackcdn.com/image/fetch/$s_!unjk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f7f52ef-c25d-4b93-b912-92b272b4e0b6_794x588.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

We would ideally want the error to behave like a well damped mass spring system given by

[](https://substackcdn.com/image/fetch/$s_!L-GX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fda57066d-b2ac-4bef-ae04-23cf0377e340_864x262.heic)

![](https://substackcdn.com/image/fetch/$s_!L-GX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fda57066d-b2ac-4bef-ae04-23cf0377e340_864x262.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

Expanding the terms in the equation, we get

[](https://substackcdn.com/image/fetch/$s_!vLzz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F144a6d5e-b38e-4aa9-9cab-ec8d53264b32_798x254.heic)

![](https://substackcdn.com/image/fetch/$s_!vLzz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F144a6d5e-b38e-4aa9-9cab-ec8d53264b32_798x254.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

Compare this to the actual system

[](https://substackcdn.com/image/fetch/$s_!9VDg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7446c7de-5c4c-4048-b854-f8c18396e7f0.heic)

![](https://substackcdn.com/image/fetch/$s_!9VDg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7446c7de-5c4c-4048-b854-f8c18396e7f0.heic)

We now get the generalized control law for tracking arbitrary trajectory tracking

[](https://substackcdn.com/image/fetch/$s_!VGB6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2684a5ca-8692-44a6-8c50-0a554672c189_876x194.heic)

![](https://substackcdn.com/image/fetch/$s_!VGB6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2684a5ca-8692-44a6-8c50-0a554672c189_876x194.heic)

We do notice that there is a double derivative term

[](https://substackcdn.com/image/fetch/$s_!RMLQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F982630ae-268e-4428-90af-73ab7ebed283.heic)

![](https://substackcdn.com/image/fetch/$s_!RMLQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F982630ae-268e-4428-90af-73ab7ebed283.heic)

to create a virtual mass effect but double derivative is a noisier operation than the derivative itself. And the characteristic equation 𝑚𝑠^2 + 𝑏𝑠+ 𝑘= 0, which can also be written as

[](https://substackcdn.com/image/fetch/$s_!3x_u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07d05460-500e-488b-9415-aac416be7552_254x62.heic)

![](https://substackcdn.com/image/fetch/$s_!3x_u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07d05460-500e-488b-9415-aac416be7552_254x62.heic)

has really only two independent parameters to tune to make𝑠 the roots in the desired location. So the double derivative term is unnecessary. It is enough if we adjust the damping coefficient and spring constant to make the roots go into the left half plane. The closed loop equation now becomes

[](https://substackcdn.com/image/fetch/$s_!MXZF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2c32f35-f473-44fe-a4c5-7f3a404d3460_656x200.heic)

![](https://substackcdn.com/image/fetch/$s_!MXZF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2c32f35-f473-44fe-a4c5-7f3a404d3460_656x200.heic)

So an implementable control law is

[](https://substackcdn.com/image/fetch/$s_!1Cgd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F024bc1f7-2513-4647-8d9e-01383cd52a68_568x50.heic)

![](https://substackcdn.com/image/fetch/$s_!1Cgd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F024bc1f7-2513-4647-8d9e-01383cd52a68_568x50.heic)

So we have the **feed forward + feedback control scheme** and believe me when I say that this is the form of the control equation even used in the sophisticated robots we have today. We can also accommodate integral action in this scheme. Putting the integral scheme

[](https://substackcdn.com/image/fetch/$s_!mHE9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff26616e-2fac-4c82-92a4-8df0dd4c063c_706x108.heic)

![](https://substackcdn.com/image/fetch/$s_!mHE9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff26616e-2fac-4c82-92a4-8df0dd4c063c_706x108.heic)

But the new characteristic equation now becomes

[](https://substackcdn.com/image/fetch/$s_!HcL8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F591001d9-dedd-4fa2-be1a-c851e094f4b1_444x64.heic)

![](https://substackcdn.com/image/fetch/$s_!HcL8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F591001d9-dedd-4fa2-be1a-c851e094f4b1_444x64.heic)

Again the advantage of the integral action scheme is that it leads to robust trajectory tracking under constant or slowly varying disturbances but again a root locus diagram would be required to decide the controller parameters for now the characteristic equation of third order results as

[](https://substackcdn.com/image/fetch/$s_!54NO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90c1dfa8-2901-4578-be92-a1837d61798e_486x62.heic)

![](https://substackcdn.com/image/fetch/$s_!54NO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90c1dfa8-2901-4578-be92-a1837d61798e_486x62.heic)

Once again a root locus diagram is required to carefully choose the gains.

------------------------------------------------------------------------

# Feedback Linearization

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1saW5rIiBmaWxsPSJub25lIiBoZWlnaHQ9IjE4IiBzdHJva2U9ImN1cnJlbnRDb2xvciIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIiBzdHJva2Utd2lkdGg9IjIiIHZpZXdib3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE4IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik0xMCAxM2E1IDUgMCAwIDAgNy41NC41NGwzLTNhNSA1IDAgMCAwLTcuMDctNy4wN2wtMS43MiAxLjcxIiAvPjxwYXRoIGQ9Ik0xNCAxMWE1IDUgMCAwIDAtNy41NC0uNTRsLTMgM2E1IDUgMCAwIDAgNy4wNyA3LjA3bDEuNzEtMS43MSIgLz48L3N2Zz4=)

There is a method to design controllers that work not only for the linear range about a set point but under the full range of the system. This topic comes under an oceanic area of “Non Linear Control” with wide arenas of complicated techniques and extensive research, for the aero thrust pendulum, it turns out to be an easy problem. Again, let us not dive into the subject of non linear control and research on what makes it so easy for our aero system and let us not attempt to generalize. But this comes under the broad umbrella of **feedback linearization** which is very simple to understand for the aero thrust pendulum. Consider the aero thrust pendulum

[](https://substackcdn.com/image/fetch/$s_!vgHe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc87f054-dc1c-4972-af7b-deada1b4ccf3_914x418.heic)

![](https://substackcdn.com/image/fetch/$s_!vgHe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc87f054-dc1c-4972-af7b-deada1b4ccf3_914x418.heic)

![](data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiBoZWlnaHQ9IjIwIiByb2xlPSJpbWciIHN0cm9rZT0idmFyKC0tY29sb3ItZmctcHJpbWFyeSkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIxLjUiIHZpZXdib3g9IjAgMCAyMCAyMCIgd2lkdGg9IjIwIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxnPjx0aXRsZT48L3RpdGxlPjxwYXRoIGQ9Ik0yLjUzMDAxIDcuODE1OTVDMy40OTE3OSA0LjczOTExIDYuNDMyODEgMi41IDkuOTExNzMgMi41QzEzLjE2ODQgMi41IDE1Ljk1MzcgNC40NjIxNCAxNy4wODUyIDcuMjM2ODRMMTcuNjE3OSA4LjY3NjQ3TTE3LjYxNzkgOC42NzY0N0wxOC41MDAyIDQuMjY0NzFNMTcuNjE3OSA4LjY3NjQ3TDEzLjY0NzMgNi45MTE3Nk0xNy40OTk1IDEyLjE4NDFDMTYuNTM3OCAxNS4yNjA5IDEzLjU5NjcgMTcuNSAxMC4xMTc4IDE3LjVDNi44NjExOCAxNy41IDQuMDc1ODkgMTUuNTM3OSAyLjk0NDMyIDEyLjc2MzJMMi40MTE2NSAxMS4zMjM1TTIuNDExNjUgMTEuMzIzNUwxLjUyOTMgMTUuNzM1M00yLjQxMTY1IDExLjMyMzVMNi4zODIyNCAxMy4wODgyIiAvPjwvZz48L3N2Zz4=)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ibHVjaWRlIGx1Y2lkZS1tYXhpbWl6ZTIgbHVjaWRlLW1heGltaXplLTIiIGZpbGw9Im5vbmUiIGhlaWdodD0iMjAiIHN0cm9rZT0iY3VycmVudENvbG9yIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBvbHlsaW5lIHBvaW50cz0iMTUgMyAyMSAzIDIxIDkiPjwvcG9seWxpbmU+PHBvbHlsaW5lIHBvaW50cz0iOSAyMSAzIDIxIDMgMTUiPjwvcG9seWxpbmU+PGxpbmUgeDE9IjIxIiB4Mj0iMTQiIHkxPSIzIiB5Mj0iMTAiPjwvbGluZT48bGluZSB4MT0iMyIgeDI9IjEwIiB5MT0iMjEiIHkyPSIxNCI+PC9saW5lPjwvc3ZnPg==)

which is a linear system with no spring effect. We have cancelled the non linear nature of gravity spring completely through non linear feedback instead of linearizing it and looking at small excursions. So controller design for the above system is simple. We can use PD or PID control for root locus design and choose w(t).

Here we make the closed loop system linear exactly through feedback. This is hence called **feedback linearization**. This is a wide class of techniques with so many generalizations and complications in non linear control. This is just the ground level example of that technique. Of course, we have to know 𝑚𝑔*l*\_𝐶𝑀 a bit accurately to do so. Controller design for w(t) is carried out in a routine manner except that 𝑘 𝑜𝑟 𝑚𝑔𝑙_𝐶𝑀 = 0 and remembering that the controller thus designed is valid in all ranges.

------------------------------------------------------------------------

Await the link to the next article in this series here.

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0iaWNvbiIgZmlsbD0iIzAwMDAwMCIgaGVpZ2h0PSIyMCIgcm9sZT0iaW1nIiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3R5bGU9ImhlaWdodDoyMHB4O3dpZHRoOjIwcHg7IiB2aWV3Ym94PSIwIDAgMjQgMjQiIHdpZHRoPSIyMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48Zz48dGl0bGU+PC90aXRsZT48c3ZnIGNsYXNzPSJsdWNpZGUgbHVjaWRlLWhlYXJ0IiBoZWlnaHQ9IjI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTE5IDE0YzEuNDktMS40NiAzLTMuMjEgMy01LjVBNS41IDUuNSAwIDAgMCAxNi41IDNjLTEuNzYgMC0zIC41LTQuNSAyLTEuNS0xLjUtMi43NC0yLTQuNS0yQTUuNSA1LjUgMCAwIDAgMiA4LjVjMCAyLjMgMS41IDQuMDUgMyA1LjVsNyA3WiIgLz48L3N2Zz4=)

3

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0iaWNvbiIgZmlsbD0iIzAwMDAwMCIgaGVpZ2h0PSIyMCIgcm9sZT0iaW1nIiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3R5bGU9ImhlaWdodDoyMHB4O3dpZHRoOjIwcHg7IiB2aWV3Ym94PSIwIDAgMjQgMjQiIHdpZHRoPSIyMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48Zz48dGl0bGU+PC90aXRsZT48c3ZnIGNsYXNzPSJsdWNpZGUgbHVjaWRlLW1lc3NhZ2UtY2lyY2xlIiBoZWlnaHQ9IjI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTcuOSAyMEE5IDkgMCAxIDAgNCAxNi4xTDIgMjJaIiAvPjwvc3ZnPg==)

![](data:image/svg+xml;base64,PHN2ZyBjbGFzcz0iaWNvbiIgZmlsbD0ibm9uZSIgaGVpZ2h0PSIyMCIgcm9sZT0iaW1nIiBzdHJva2U9InZhcigtLWNvbG9yLWZnLXByaW1hcnkpIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiIHN0cm9rZS13aWR0aD0iMiIgdmlld2JveD0iMCAwIDIwIDIwIiB3aWR0aD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGc+PHRpdGxlPjwvdGl0bGU+PHBhdGggZD0iTTIuNTMwMDEgNy44MTU5NUMzLjQ5MTc5IDQuNzM5MTEgNi40MzI4MSAyLjUgOS45MTE3MyAyLjVDMTMuMTY4NCAyLjUgMTUuOTUzNyA0LjQ2MjE0IDE3LjA4NTIgNy4yMzY4NEwxNy42MTc5IDguNjc2NDdNMTcuNjE3OSA4LjY3NjQ3TDE4LjUwMDIgNC4yNjQ3MU0xNy42MTc5IDguNjc2NDdMMTMuNjQ3MyA2LjkxMTc2TTE3LjQ5OTUgMTIuMTg0MUMxNi41Mzc4IDE1LjI2MDkgMTMuNTk2NyAxNy41IDEwLjExNzggMTcuNUM2Ljg2MTE4IDE3LjUgNC4wNzU4OSAxNS41Mzc5IDIuOTQ0MzIgMTIuNzYzMkwyLjQxMTY1IDExLjMyMzVNMi40MTE2NSAxMS4zMjM1TDEuNTI5MyAxNS43MzUzTTIuNDExNjUgMTEuMzIzNUw2LjM4MjI0IDEzLjA4ODIiIC8+PC9nPjwvc3ZnPg==)

2

Share
