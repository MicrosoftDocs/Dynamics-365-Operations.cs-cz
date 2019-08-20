---
title: Osobní výdaje ve vyúčtování výdajů
description: Toto téma vysvětluje dvě metody pro zpracování osobních výdajů zaměstnance v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794975"
---
# <a name="personal-expenses-on-an-expense-report"></a>Osobní výdaje v sestavě výdajů

[!include [banner](../includes/banner.md)]

Během služební cesty může dojít k tomu, že zaměstnanec zaplatí osobní výdaje kreditní kartou společnosti. Pokud není definovaný proces pro osobní výdaje, může být schválení vyúčtování výdajů přerušeno, když zaměstnanec odevzdá rozpis vyúčtování výdajů. 

V aplikaci Microsoft Dynamics 365 for Finance and Operations existují dvě metody pro zpracování osobních výdajů zaměstnance:

- **Zaplaceno zaměstnancem** – Vaše organizace neplatí osobní výdaje, které se objevují na výpisu platební karty společnosti. Místo toho se vytváří sestava zobrazující osobní výdaje společně s firemními výdaji, které byly zaúčtovány na platební kartu společnosti.
- **Placené společností** – Společnost proplatí všechny položky na výpisu z kreditní karty a potom zatíží účet pracovníka částkou osobních výdajů.

Na stránce **Parametry správy výdajů** můžete vybrat metodu, kterou používá vaše organizace.
