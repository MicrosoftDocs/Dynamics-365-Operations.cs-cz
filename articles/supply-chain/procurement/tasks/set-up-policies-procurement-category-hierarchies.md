--- 
title: "Nastavení zásad pro hierarchie kategorií zásobování"
description: "Tento postup použijte k nastavení pravidel pro objednávání produktů v kategorii."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 50764f99be04d27e04047824f870e724336cb452
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Nastavení zásad pro hierarchie kategorií zásobování

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup použijte k nastavení pravidel pro objednávání produktů v kategorii. Pravidla jsou definována pro určitou zásadu nákupu. Pravidlo zásad přístupu ke kategorii určuje, ke kterým kategoriím zásobování mají uživatelé přístup při vytváření žádanky. Při vytvoření žádanky jsou zásada nákupu a pravidla přístupu ke kategoriím určená k použití určena na základě právního subjektu a provozní jednotky, do které zaměstnanec patří. Tento postup můžete projít v ukázkových datech společnosti USMF. Tento úkol obvykle provádí manažer nákupu.


## <a name="find-the-procurement-policy"></a>Vyhledejte zásady zásobování
1. Přejděte na Zásobování a zdroje > Nastavení > Zásady > Zásady nákupu.
2. Klepněte na odkaz u USMF – zásady zásobování.
    * Toto je zásada, ke které přidáte pravidlo. Musí být aktivní zásadou.  

## <a name="create-a-category-access-rule"></a>Vytvořit pravidlo přístupu ke kategorii
1. Vyberte pravidlo zásad přístupu ke kategorii.
    * Pokud je tlačítko Vytvořit pravidlo zobrazeno šedě, je to proto, že již existuje aktivní pravidlo zásad pro přístup ke kategorii. Zkontrolujte pole Účinné datum a Datum vypršení platnosti, určete, které z nich to je, vyberte je a klepněte na tlačítko Vyřadit pravidlo zásad. Pokud je tlačítko Vytvořit pravidlo zásad k dispozici, nemusíte provádět žádné změny.  
2. Klikněte na Vytvořit pravidlo zásad.
3. Do pole Datum platnosti zadejte datum a čas.
    * Čas se nesmí překrývat s dalším pravidlem, které je již aktivní.  
    * Vyberte kategorii, pro kterou bude pravidlo platit. Poznamenejte si, o jakou kategorii se jedná – budete ji potřebovat později. Při výběru kategorie se do vybraného seznamu kategorií přidají její kategorie nebo nadřazené kategorie.  
    * Vyberte možnost Zahrnout podkategorie, chcete-li pravidlo použít na všechny podkategorie vybrané kategorie.  
4. Klepněte na možnost Přidat.
    * Pokud nastavíte možnost Zahrnout nadřazené pravidlo na Ano, pravidlo zásad, které definujete pro nadřazené kategorie, bude také přiřazeno podřízeným kategoriím, pokud nebylo žádné pravidlo zásad definováno pro podřízené kategorie.  
5. Klikněte na tlačítko OK.

## <a name="create-a-category-policy-rule"></a>Vytvořit pravidlo zásad kategorie
1. Vyberte pravidlo zásad kategorie
    * Pokud je tlačítko Vytvořit pravidlo zásad zobrazeno šedě, vyberte aktivní pravidlo zásad a klepněte na tlačítko Vyřadit pravidlo zásad.  
2. Klikněte na Vytvořit pravidlo zásad.
3. Do pole Datum platnosti zadejte datum a čas.
4. Klepněte na možnost Přidat.
5. Vyberte stejnou kategorii, která je použita pro pravidlo přístupu ke kategorii.
6. Vyberte možnost v poli Výběr dodavatele.
    * Vyberte pravidlo, které určuje, jaký typ dodavatelů lze vybrat pro kategorii při vytváření žádanky.  
7. Klikněte na tlačítko Zavřít.
    * Vámi definovaná pravidla zásad, byla pro žádanky typu Spotřeba. Pokud chcete definovat zásady pro žádanky typu Doplnění, vytvořte pravidlo pro typ pravidla zásad s názvem „Pravidlo zásad přístupu ke kategorii doplnění“.  


