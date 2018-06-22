---
title: "Generování sestavy přidáním obsahu v podobě neformátovaného dokumentu XML"
description: "Formáty v modulu Elektronické výkaznictví (ER) můžete navrhovat pro generování odchozích dokumentů ve formátu XML."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: af594fb7879918e6b9fc423774ee1ec7f635dec0
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2018

---

# <a name="generate-er-reports-by-adding-content-as-raw-xml"></a>Generování sestav ER přidáním obsahu v podobě neformátovaného dokumentu XML

[!include[banner](../includes/banner.md)]

Můžete použít nový prvek formátu **RAW XML** k návrhu formátů elektronických sestav (ER), které generují odchozí dokumenty ve formátu XML. V některých případech budete pravděpodobně chtít přidat data XML k těmto sestavám, z jednoho nebo více z následujících důvodů:

- Je praktičtější použít neformátovaný dokument XML pro původní návrh a průběžnou údržbu sestav, vzhledem k tomu, že struktura jazyka XML může být automaticky generována spuštěním výrazu runtime. Proto není nutné v době návrhu určovat více vazeb pro prvky ve více formátech. To je možné, když zdroje dat, které používáte, obsahují informace, které lze použít k vytvoření prvků XML, když je generovaná sestava. 
- Žádný jiný způsob nelze použít pro zadání sestavy s obsahem XML, který byl předtím přijat a uložen v systému. Například generovaná odpověď XML by mohla nutně obsahovat obsah požadavku XML, který byl odeslán předtím.
- Nelze použít žádnou jinou metodu k vkládání znaků do generovaného dokumentu na základě jeho číselných kódů. Pro některé jazyky a znaky neexistují kódy tohoto typu. Mezi příklady patří řecké písmeno (ρ) a kódy entity HTML jako \&eacute; pro dlouhé *e* (é).

> [!NOTE]
> Počítejte s tím, že systém neřídí, zda je obsah XML, který se umístí do vygenerovaného dokumentu pomocí prvku formátu **RAW XML*** správný.

Další informace o této funkci získáte přehráním průvodců záznamů úlohy **ER Použití nezpracovaných dat XML ke generování sestav XML (část 1: Návrh datového modelu)** a **ER Použití nezpracovaných dat XML ke generování sestav XML (část 2: Návrh a spuštění sestavy)**, které jsou součástí obchodního procesu **7.5.4.3 Acquire/Develop IT service/solution components (10677)** a dají se stáhnout ze [služby Stažení softwaru Microsoft](https://go.microsoft.com/fwlink/?linkid=874684). Tito průvodci záznamem úloh vás provedou procesem konfigurace formátu ER k vložení nezpracovaných dat XML do generovaných souborů.

