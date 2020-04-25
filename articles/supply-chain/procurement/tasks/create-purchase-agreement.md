---
title: Vytvoření nákupní smlouvy
description: Toto téma vás provede vytvořením nákupní smlouvy.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207731"
---
# <a name="create-a-purchase-agreement"></a>Vytvoření nákupní smlouvy

[!include [banner](../../includes/banner.md)]

Toto téma vás provede vytvořením nákupní smlouvy. Toto by obvykle prováděl vedoucí nákupu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Než začnete, je třeba nastavit klasifikace nákupní smlouvy. Vytvořenou smlouvu můžete použít při vytváření nákupní objednávky; tím se zkopírují podmínky nákupní smlouvy do záhlaví a jakýchkoli řádků objednávky ovlivněných touto smlouvou.


## <a name="create-a-new-purchase-agreement"></a>Vytvoření nové nákupní smlouvy
1. Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Nákupní smlouvy > Nákupní smlouvy**.
2. Klepněte na možnost **Nový**.
3. V poli **Účet dodavatele** vyberte rozevírací nabídku a zvolte řádek požadovaného záznamu.
4. V poli **Klasifikace nákupní smlouvy** vyberte rozevírací nabídku a zvolte řádek požadovaného záznamu.
5. Rozbalte pevnou záložku **Obecné**.
6. Do pole **Datum vypršení platnosti** zadejte datum.

    - Toto datum vypršení platnosti bude výchozí pro všechny řádky závazků a určí, jak dlouho budou jednotlivé závazky platné.  

7. V poli **Název dokumentu** zadejte název nákupní smlouvy.

    - Ponechejte pole **Výchozí závazek** nastavené na hodnotu **Závazek – množství produktu** (nebo pokud je nastavená jiná hodnota, změňte ji).  
    - Výchozí hodnota závazku určuje možnosti na řádcích smlouvy. Pokud potřebujete nový typ závazku při vytváření řádků smlouvy, je nutné změnit výchozí závazek v záhlaví. Jsou k dispozici 4 typy závazků: **Závazek – množství produktu** pro určité množství produktu; **Závazek – hodnota produktu** pro konkrétní částku měny pro produkt; **Závazek – hodnota kategorie produktu** pro konkrétní částku měny v kategorii zásobování, kde částka může být pro katalogovou položku nebo nekatalogovou položku; **Závazek ohledně hodnoty** pro konkrétní částku měny, která může být splněna jakýmkoli produktem nebo jakoukoli kategorií zásobování.  

8. Vyberte **OK**.

## <a name="add-a-commitment"></a>Přidání závazku
1. Vyberte **Přidat řádek**.
2. V poli **Číslo položky** vyberte z rozevírací nabídky požadovaný záznam.
3. Zadejte číslo do pole **Množství**. Toto je celkového množství, které podle dohody zakoupíte od dodavatele.  
4. Zadejte číslo do pole **Jednotková cena**.
5. Rozbalte sekci **Podrobnosti řádku**.
6. Nastavte možnost **Max je vynuceno** na hodnotu **Ano**. Možnost **Max je vynuceno** omezuje použití závazku. Můžete produkt zakoupit pouze do množství zadaného v poli **Množství** pro daný řádek.  

## <a name="add-header-conditions"></a>Přidání podmínek záhlaví
1. V podokně akcí vyberte **Možnosti**.
2. Vyberte **Změnit zobrazení**.
3. Vyberte **Zobrazení záhlaví**.
4. Rozbalte část **Podmínky**.
5. V poli **Metoda platby** vyberte požadovaný záznam v rozevírací nabídce. Zde jsou ve výchozím nastavení zobrazené platební podmínky z účtu dodavatele.  
6. V poli **Způsob dodání** vyberte požadovaný záznam v rozevírací nabídce.
7. V poli **Dodací podmínky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.

## <a name="confirm-and-activate-the-agreement"></a>Potvrzení a aktivace smlouvy
1. V podokně akcí klikněte na možnost **Nákupní smlouva**.
2. Vyberte **Potvrzení**. Nastavte možnost **Označit smlouvu jako platnou** na hodnotu **Ano**.  
3. Vyberte **OK**.
4. V podokně akcí klikněte na možnost **Nákupní smlouva**.
5. Zvolte **Potvrzení nákupní smlouvy**. Možnost **Náhled/tisk** umožňuje generovat dokument pro nákupní smlouvu, který pak můžete vytisknout nebo odeslat dodavateli. Pokud smlouvu aktualizujete a znovu potvrdíte později, zobrazí se zde obě verze.  
6. Zavřete stránku.

