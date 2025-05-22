# 暖かい日記 (Nuan-kaiRi-Ji)

!<img src="https://github.com/user-attachments/assets/09ccc812-3460-4ea4-81eb-fb64cbea3e3b width="200" height="200"/>


## 📖 プロジェクト紹介 / Project Overview

**日本語**  
**暖かい日記**は、高齢者のために設計されたAI搭載の対話型日記・リマインダーWebアプリです。

- ユーザーは雲のキャラクターと自然な会話をしながら、日常・健康・服薬・予定などの情報を優しく簡単に記録できます。
- チャットボットは会話中に重要な予定や服薬情報を自動検出し、リマインダーとして登録します。また、日常会話は自動で「日記」として要約・保存されます。
- 「記憶クイズ」機能では、AIがユーザーのリマインダーや過去の出来事について質問し、認知力の維持・向上をサポートします。
- 緊急連絡先やプロフィール、病院情報も一目で確認できるなど、高齢者の安心と家族の見守りを両立します。
- **高齢者にやさしいUI**（大きな文字・明るい配色・シンプルな構成・タッチ最適化）で、誰でも簡単に使えます。
- "実はこのキャラクター、雲じゃなくて…脳なんです！🧠（笑）"

**English**  
**Nuan-kaiRi-Ji** is an AI-powered, interactive diary and reminder web app designed for older adults.

- Users can interact with a friendly cloud character and easily record daily life, health, medication, and schedules through natural conversation.
- The chatbot automatically detects important events or medication instructions during conversations and registers them as reminders. Daily chats are automatically summarized and saved as "journals."
- The "Memory Quiz" feature helps users maintain and improve cognitive skills by asking questions about their reminders or past events.
- Emergency contacts, profile, and hospital information are always accessible, supporting both user safety and family peace of mind.
- **Senior-friendly UI**: Large text, bright colors, simple layout, and touch optimization make it easy for anyone to use.
- "Surprise: our cute 'cloud' is... really a brain! 🧠"

---

## 🌟 主な機能 / Key Features

- **AIチャットボット** / AI chatbot: 雲キャラクターとの自然な対話 / Natural conversation with a cloud character
- **リマインダー自動検出** / Automatic reminder detection: 会話中に予定や服薬を自動登録 / Detects and registers reminders during chat
- **日記自動生成** / Auto journal creation: 会話内容を要約し日記として保存 / Summarizes chats as journals, viewable anytime
- **記憶クイズ** / Memory quiz: AIがリマインダーや日常情報でクイズを出題 / AI quizzes based on reminders and daily info
- **緊急連絡先管理** / Emergency contact management: 家族・医師の連絡先を簡単管理・修正 / Manage and edit family/doctor contacts
- **プロフィール管理** / Profile management: 血液型・持病・住所などの情報登録 / Manage blood type, medical history, address, etc.
- **高齢者向けUI** / Senior-friendly UI: 大きな文字・明るい色・タッチ最適化 / Large fonts, bright colors, touch-optimized

---

## 🛠 技術スタック / Tech Stack

- **フロントエンド / Frontend**: React, CSS Modules, モバイルファースト / Mobile-first design
- **バックエンド / Backend**: RESTful API (Node.js/Flask etc.)
- **AI・大規模言語モデル / AI・LLM**:  
  - Ollamaサーバー上で動作する**Qwen2.5**シリーズのLLM（現在は5Bパラメータモデル）  
  - Ollama server running Qwen2.5 LLM (currently 5B parameters)
- **データベース / Database**: SQLite/MySQL  
  (users, emergency_contacts, journals, reminders, messages etc.)

---

## 🔗 リポジトリ / Repositories

- [FRONT-END REPO](https://github.com/Mosic-asia/Project-kiokuSupportService-react-repo)
- [BACK-END REPO](https://github.com/Mosic-asia/kioku)

---

## 📚 主なAPI・DB設計 / Main API & DB Design

- **チャット / Chat**:  
  - `GET /api/users/<user_id>/chat/start`  
  - `POST /api/users/<user_id>/chat/continue`  
  - `POST /api/users/<user_id>/chat/summarize`  
  - `POST /api/users/<user_id>/chat/end`
- **記憶クイズ / Memory Quiz**:  
  - `POST /api/users/<user_id>/memory-quiz`
- **日記 / Journal**:  
  - `GET /api/users/<user_id>/journals`  
  - `GET /api/users/<user_id>/journals/<conversation_id>`
- **緊急連絡先 / Emergency Contacts**:  
  - `GET /api/users/<user_id>/emergency_contacts`  
  - `PATCH /api/users/<user_id>/emergency_contacts/<id>`
- **プロフィール / Profile**:  
  - `GET /api/users/<user_id>`  
  - `PATCH /api/users/<user_id>`
- **DBテーブル / DB Tables**:  
  - users, emergency_contacts, reminders, journals, messages, photo_memos

---

## 🎯 プロジェクトの目的 / Project Purpose

**日本語:**  
高齢者が「日々を記録し、服薬や予定を管理し、心のつながりや認知力を保つ」ことを  
誰でも簡単・安心・あたたかく実現できることを目指しています。

**English:**  
Our goal is to help older adults easily, warmly, and safely  
record daily life, manage medication/schedules, maintain social connection, and support cognitive health.

---

## 📎 参考 / References

- [API仕様書 / API Specification (PDF)](./Memory-App-API-Specification-AI-API-Specification.pdf)
- [DBテーブル設計 / DB Table Design (PDF)](./Memory-App-API-Specification-Database-tables.pdf)
- [UIシナリオ画像 / UI Scenario Image](https://pplx-res.cloudinary.com/image/private/user_uploads/71039046/b8b597c3-c34c-42d4-a7ea-fa89c9ca2115/Nuan-kaiRi-Ji-1.jpg)

---

### コミットルール / Commit Rule : [Gitmoji](https://gitmoji.dev/)

- npm i -g gitmoji-cli     
- gitmoji -c
