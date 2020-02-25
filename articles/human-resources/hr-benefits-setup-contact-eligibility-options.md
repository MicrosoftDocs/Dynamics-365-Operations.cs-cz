---
title: Konfigurace možností způsobilosti osobních kontaktů
description: Nakonfigurujte možnosti způsobilosti osobních kontaktů v Microsoft Dynamics 365 Human Resources. Osobními kontakty mohou být osoby, které jsou příjemci nebo závislé osoby.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008377"
---
# <a name="configure-personal-contact-eligibility-options"></a>Konfigurace možností způsobilosti osobních kontaktů

[!include [banner](includes/preview-feature.md)]

Tento článek vysvětluje, jak konfigurovat typy osobních kontaktů, které mají být použity ve výhodách v aplikaci Microsoft Dynamics 365 Human Resources. Osobními kontakty mohou být osoby, které jsou příjemci nebo závislé osoby. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Možnosti nároků na osobní kontakty**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Možnost způsobilosti** | Jedinečný název nebo kód možnosti nároku pro identifikaci možnosti nároku. |
   | **Popis** | Stručný popis možnosti nároku. |
   | **Kód způsobilosti kontaktu** | Systémový kód, který nejlépe popisuje možnost osobní způsobilosti. Lze vybrat následující možnosti: <ul><li>Vztah</li><li>Student</li><li>Rodinný příslušník nad věkovým limitem</li><li>Rodinný příslušník s postižením nad věkovým limitem</li></ul> |
   | **Stav** | Stav možnosti nároku. Pokud je stav možnosti nároku nastaven na neaktivní, nemůžete vybrat možnost nároku na osobní kontakt pro osobní kontakty. |
   | **Vztah** | Určuje vztah mezi osobním kontaktem a zaměstnancem. Toto pole je aktivní pouze v případě, že je kód nároku na kontakt nastavený na vztah. |
   | **Věk** | Maximální stáří vhodného osobního kontaktu pro plán zaměstnaneckých výhod. Toto pole je aktivní pouze v případě, že vyberete vztah. Tento věk se porovnává s vypočítaným stářím osobního kontaktu. Vypočítaný věk je: (datum disponibility – datum narození osobního kontaktu / 365). Toto číslo je vždy celé číslo. |

4. Zvolte **Uložit**. 
