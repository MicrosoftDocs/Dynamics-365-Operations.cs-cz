---
title: Nastavení storna deníků a řádků
description: Toto téma se zabývá důvodem, proč storno záznam, který byl zadán do hlavního deníku, nemusel být zahrnut do zaúčtované transakce.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff8c0bda8e750e95261039b373cfb96a76034f6f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724438"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Nastavení storna deníků a řádků

[!include [banner](../includes/banner.md)]

Toto téma se zabývá důvodem, proč storno záznam, který byl zadán do hlavního deníku, nemusel být zahrnut do zaúčtované transakce.  

## <a name="symptom"></a>Příznak

Hlavní deník zahrnuje storno záznam a datum stornování v deníku. Když deník zaúčtujete, nestornuje se žádný doklad. Proč tomu tak je?

## <a name="resolution"></a>Řešení

Když se deník zaúčtovává, proces stornování se dívá pouze na nastavení **Storno záznamu** a **Datum stornování** v části **Řádky** dokladu. Tento přístup umožňuje deníku zahrnout některé doklady, které jsou označeny ke stornování, a jiné, které tak označeny nejsou.

Hodnoty z deníku se při přidávání řádků jako *Nový* použijí pouze jako výchozí. Změna hodnot v deníku neovlivňuje existující řádky. V tomto příkladu byly nejprve zadány řádky dokladů. Když zadáte podrobnosti řádku před označením deníku jako stornování, označení jako storno záznamu a datum stornování se nepoužije na žádné existující řádky.

Změna storno záznamu nebo data stornování na existujícím řádku šíří tuto změnu na další řádky ve stejném dokladu. K optimalizaci výkonu se mřížka po šíření změn na jiné řádky neaktualizuje. Aktualizované hodnoty můžete zobrazit aktualizováním mřížky.


