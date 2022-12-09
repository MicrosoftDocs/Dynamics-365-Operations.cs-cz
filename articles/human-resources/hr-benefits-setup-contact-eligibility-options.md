---
title: Konfigurace možností způsobilosti osobních kontaktů
description: Tento článek vysvětluje, jak konfigurovat možnosti způsobilosti osobních kontaktů v Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e3e393002901f31c035a54bd8036ed20ecdf9e00
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803876"
---
# <a name="configure-personal-contact-eligibility-options"></a>Konfigurace možností způsobilosti osobních kontaktů


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek vysvětluje, jak konfigurovat typy osobních kontaktů, které mají být použity ve výhodách v aplikaci Microsoft Dynamics 365 Human Resources. Osobní kontakty jsou jednotlivci, na které se budou vztahovat vaše plány (závislé osoby) nebo kteří budou mít prospěch z vašich plánů (příjemci). Závislými osobami jsou obvykle manželé nebo děti. Příjemci mohou být manželé, děti, svěřenské fondy nebo rodiče.

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
   | **Věk** |Určuje maximální stáří vhodného osobního kontaktu pro plán zaměstnaneckých výhod. Toto pole je aktivní pouze v případě, že vyberete vztah. Tento věk se porovnává s vypočítaným stářím osobního kontaktu. Vypočítaný věk je: (datum disponibility – datum narození osobního kontaktu / 365). Toto číslo je vždy celé číslo.
V případě možnosti způsobilosti kontaktu **Překročení věku závislé osoby** je věk v tomto poli minimální věk. Například: pokud je u možnosti **Překročení věku závislé osoby** věk nastaven na 18, možnost způsobilosti se bude vztahovat na závislé osoby, které jsou označeny jako překročení věku závislé osoby a jsou starší 18 let.  |

4. Zvolte možnost **Uložit**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
