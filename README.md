# iPhone 锁屏倒计时 & 壁纸生成器

本项目是一个简单的静态网页，用于生成带有倒计时、日期和日程表的自定义 iPhone 锁屏壁纸。壁纸上会醒目地显示一个目标日期的倒计时，以及一系列预定事件或提醒。
This project is a simple static webpage designed to generate custom iPhone lock screen wallpapers with a countdown, date, and schedule integration. The wallpaper prominently displays a countdown towards a specified date along with a list of scheduled events or reminders.

## 功能
- 自定义目标日期的倒计时。
- 显示带有时间、标题和地点的日程事件。
- 可自定义的壁纸背景色和文字颜色。
- 预设的莫兰迪色系自适应配色方案。

## 使用说明

### 开始使用
要使用倒计时和壁纸生成器，您可以通过 URL 查询参数进行自定义。这些参数允许您设置标题、目标日期、颜色方案并添加自定义日程。

### URL 参数

以下参数可以在 URL 的查询字符串中使用，以配置生成的壁纸：

| 参数               | 描述                                                                                   | 必填   | 示例                                              |
| ------------------ | -------------------------------------------------------------------------------------- | ------ | ------------------------------------------------- |
| `title`            | 壁纸顶部显示的标题。                                                                    | 可选   | `我的倒计时`                                      |
| `date`             | 倒计时的目标日期（格式：`YYYY-MM-DD`）。                                                | 必填   | `2024-12-31`                                      |
| `body_color`       | 壁纸的背景色（HEX 格式）。如果未指定，将随机使用颜色。                                  | 可选   | `#EBD8D1`                                         |
| `title_color`      | 标题区域的背景色（HEX 格式）。                                                          | 可选   | `#6D6D75`                                         |
| `title_text_color` | 标题区域文字的颜色（HEX 格式）。                                                        | 可选   | `#FFFFFF`                                         |
| `schedule`         | 事件安排的 JSON 编码数组。每个项目包含标题、时间、地点等信息。                           | 可选   | `[{"title":"会议", "time_top":"14:00", "time_bottom":"15:00", "location":"办公室"}]` |

### 日程结构

`schedule` 参数应包含 JSON 编码的事件对象数组。每个事件对象可以包含以下字段：

| 字段           | 描述                                                                 | 必填   | 示例                           |
| -------------- | -------------------------------------------------------------------- | ------ | ------------------------------ |
| `title`        | 事件或提醒的标题。                                                    | 必填   | `项目截止日期`                 |
| `time_top`     | 事件的开始时间。                                                      | 可选   | `09:00 AM`                     |
| `time_bottom`  | 事件的结束时间。                                                      | 可选   | `10:00 AM`                     |
| `time_big`     | 大字体显示倒计时（用于突出剩余天数）。                                | 可选   | `5`                            |
| `location`     | 事件的地点。                                                          | 可选   | `101 会议室`                   |

### 示例

以下是一个如何使用查询参数的示例：

```plaintext
https://rlxzmdd.github.io/PhoneDays/?title=事件倒计时&date=2024-12-25&body_color=#E5D3B3&title_color=#4B5262&title_text_color=#F8F8F8&schedule=[{"title":"团队会议","time_top":"14:00","time_bottom":"15:00","location":"办公室"}]
```
在这个示例中，页面将显示一个倒计时到 2024 年 12 月 25 日的壁纸，使用自定义的颜色方案，并为 “团队会议” 显示一个事件。

### 自定义
1.	颜色：如果未提供 body_color、title_color 或 title_text_color，生成器将使用随机的莫兰迪色系来设置壁纸样式。您可以指定任意 HEX 颜色格式（例如 #FFFFFF 代表白色）。
2.	日程：您可以通过编码为 JSON 的方式添加多个日程项。如果未提供日程，页面将只显示倒计时和日期。

### 部署
您可以通过任何静态网站托管服务（如 GitHub Pages、Vercel 或 Netlify）来部署该项目。只需托管 HTML 文件并通过带有查询参数的 URL 访问该页面。

### 在iPhone上运行
通过快捷指令进行运行，快捷指令获取链接：https://www.icloud.com/shortcuts/e3b66a9195d040a58e210acf610cb776

### 效果演示
![image](https://github.com/user-attachments/assets/85c5389b-e9a2-411e-adf2-33be897392b0)
<img width="391" alt="image" src="https://github.com/user-attachments/assets/7f5ee83d-95c5-45fb-bbb6-afd13bbbb2d8">


# English

## Features
- Custom countdown until a target date.
- Display scheduled events with time, title, and location.
- Customizable colors for the wallpaper background and text.
- Adaptive color scheme with pre-selected Morandi color palettes.

## Usage Instructions

### Getting Started
To use the countdown and wallpaper generator, you can pass URL query parameters to customize the output. These parameters allow you to set the title, target date, color schemes, and add custom schedules.

### URL Parameters

The following parameters can be used in the query string of the URL to configure the output:

| Parameter          | Description                                                                               | Required | Example                                           |
| ------------------ | ----------------------------------------------------------------------------------------- | -------- | ------------------------------------------------- |
| `title`            | The title displayed at the top of the wallpaper.                                           | Optional | `My Countdown`                                    |
| `date`             | The target date for the countdown (format: `YYYY-MM-DD`).                                  | Required | `2024-12-31`                                      |
| `body_color`       | The background color of the wallpaper (in HEX format). If not specified, random colors are used. | Optional | `#EBD8D1`                                         |
| `title_color`      | The background color of the title area (in HEX format).                                    | Optional | `#6D6D75`                                         |
| `title_text_color` | The text color of the title area (in HEX format).                                          | Optional | `#FFFFFF`                                         |
| `schedule`         | A JSON-encoded array of schedule items. Each item includes title, time, location, etc.     | Optional | `[{"title":"Meeting", "time_top":"14:00", "time_bottom":"15:00", "location":"Office"}]` |

### Schedule Structure

The `schedule` parameter should contain a JSON-encoded array of event objects. Each event object can contain the following fields:

| Field         | Description                                                         | Required | Example                       |
| ------------- | ------------------------------------------------------------------- | -------- | ----------------------------- |
| `title`       | The title of the event or reminder.                                  | Required | `Project Deadline`            |
| `time_top`    | The start time of the event.                                         | Optional | `09:00 AM`                    |
| `time_bottom` | The end time of the event.                                           | Optional | `10:00 AM`                    |
| `time_big`    | Large display for the countdown (used for highlighting days left).   | Optional | `5`                           |
| `location`    | The location of the event.                                           | Optional | `Room 101`                    |
