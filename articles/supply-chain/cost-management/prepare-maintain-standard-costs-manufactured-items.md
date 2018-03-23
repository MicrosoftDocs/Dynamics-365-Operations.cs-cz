---
title: "Postup přípravy na správu standardních nákladů pro vyráběné položky"
description: "Toto téma popisuje kroky pro přípravu správy nákladů pro vyráběné položky."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: c1942d1f2c8eeb05a6cbaddd2d7911a93b7e05a1
ms.contentlocale: cs-cz
ms.lasthandoff: 03/07/2018

---


# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Postup přípravy na správu standardních nákladů pro vyráběné položky

[!include[banner](../includes/banner.md)]

Toto téma popisuje kroky pro přípravu správy nákladů pro vyráběné položky. Kroky pro vyrobené položky se mírně liší od kroků pro zakoupené položky.

Zásady přiřazené vyráběným položkám mohou mít vliv na výpočty nákladů pro nadřazené vyráběné položky. Chcete-li připravit na správu nákladů vyráběných položek, postupujte podle těchto kroků.

1. Přiřaďte k vyráběné položce skupinu modelů položky. 

   Skupina modelů položky identifikuje použití standardních nákladů.

2. Přiřaďte k vyráběné položce skupinu položek. 

   Skupina položek obsahuje účty hlavní knihy, které se týkají vyráběné položky. Účty hlavní knihy pro vyráběnou položku se standardním modelem skladových nákladů zahrnují několik výrobních odchylek, odchylku změn nákladů a přecenění nákladů skladu.

3. Přiřaďte k položce měrnou jednotku zásob. 

   Náklady položky jsou vždy vyjádřeny v měrných jednotkách zásob pro danou položku.

4. Nepřiřazujte nákladovou skupinu k vyráběné položce, s výjimkou případů, kdy tato položka bude zpracována jako zakoupená položka.

5. Přiřaďte k vyráběné položce skupinu výpočtu kusovníku. 

   Skupina výpočtu kusovníku položek definuje podmínky použitých upozornění. Tímto způsobem lze po provedení výpočtu kusovníku vygenerovat zprávy s upozorněním o možných zdrojích chyb výpočtu. Zpráva s upozorněním může například upozornit na situaci, kdy neexistuje aktivní kusovník nebo postup. Skupina výpočtů kusovníku obsahuje zásadu pro zastavení rozpadu, která určuje, kdy má být vyrobená položka zpracována jako zakoupená položka.

6. Přiřaďte k vyráběné položce standardní množství objednávky, pokud má vyráběná položka konstantní náklady. 

   Standardní množství objednávky je velikost účetní šarže pro amortizaci konstantních nákladů. Příklady konstatních nákladů zahrnují časy nastavení v operacích postupu a konstantní množství komponent v kusovníku.

7. Definujte kusovník pro vyráběnou položku. 

   Pro vyráběnou položku může být definována jedna nebo více verzí kusovníku. Ověřte, zda požadované verze byly označeny jako schválené a aktivní, a zda mají požadovaná efektivní data. Verze kusovníku může být platná pro celou společnost nebo pouze pro specifické pracoviště.

8. Definujte postup pro vyráběnou položku. 

   Pro vyráběnou položku může být definována jedna nebo více verzí postupu. Ověřte, zda požadované verze byly označeny jako schválené a aktivní, a zda mají požadovaná efektivní data. Verze postupu musí být specifická pro určité pracoviště.

Pokud chcete použít informace o postupu pro účely nákladů, jsou vyžadovány dodatečné přípravné kroky. Jako příklad lze uvést kategorie nákladů přiřazené k operacím postupu - musí být správné a úplné.

<a name="related-topics"></a>Související témata
--------

[Amortizace konstantních nákladů na vyráběnou položku](amortize-constant-costs-manufactured-item.md)

[Nastavení produktů, které mohou být vyrobeny nebo pořízeny](manufactured-items-treated-as-purchased-items.md)


