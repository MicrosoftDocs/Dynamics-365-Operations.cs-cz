---
title: "Vykazování daně z prodeje pro Českou republiku"
description: "Toto téma uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku."
author: LizaGolub
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxGroup, VendParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1696023
ms.search.region: Czech Republic
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 51b033915e3d3746962249e13a7725d1acb286c4
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-reporting-for-the-czech-republic"></a>Vykazování daně z prodeje pro Českou republiku

Toto téma uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku. 

Když právnické osoby, které mají svou primární adresu v České republice, nakupují od členských států Evropské unie (EU), měly by provést vlastní vyměření daně z přidané hodnoty (DPH), aby se zajistilo, že jsou splněny následující podmínky:

-   DPH na výstupu se platí v období DPH, kdy byla vystavena faktura (datum dokumentu).
-   DPH na vstupu nebyla odečtena před přijetím dokumentu (datum rejstříku DPH).

Informace o intrakomunitární DPH mohou být vypočteny a zaúčtovány automaticky. Při zaúčtování faktury dodavatele v Evropské unii (EU) jsou vytvořeny dvě transakce DPH ve stejné výši. Jedna transakce DPH je vytvořena pro závazek prodejní daně a druhá pro pohledávku prodejní daně. Aby se tento požadavek projevil v aplikaci Microsoft Dynamics 365 for Finance and Operations, je třeba nastavit následující položky:

-   Zaškrtněte políčko **DPH intrakomunitárního plnění** na stránce **Parametry závazků** (**Závazky** &gt; **Nastavení** &gt; **Parametry závazků**).
-   Zaškrtněte políčko **Datum dokumentu pro intrakomunitární DPH** na stránce **Parametry závazků**.
-   Vytvořte dva kódy daně z prodeje: jeden, který má kladné procento daně z prodeje a druhý, který má záporné procento daně z prodeje.
-   Vytvořte skupinu daně z prodeje obsahující kladné i záporné kódy daně z prodeje. Pro záporný kód daně z prodeje vyberte parametr **DPH intrakomunitárního plnění**.
-   V denících vyberte parametr **Datum dokumentu pro intrakomunitární DPH**.

Při zaúčtování nákupní faktury, pohledávka DPH a závazek DPH jsou účtovány ve stejnou dobu. V případě kladných transakcí daně z prodeje je datum registru DPH nastaveno na datum registru DPH ze stránky zaúčtování faktury a směrování daně z prodeje je **DPH na vstupu**. V případě záporných transakcí daně z prodeje je datum registru DPH nastaveno na datum dokumentu a směrování daně z prodeje je **DPH na výstupu**.


