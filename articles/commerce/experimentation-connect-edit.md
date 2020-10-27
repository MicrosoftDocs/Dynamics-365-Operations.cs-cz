---
title: Připojení experimentu a úpravy variant
description: Toto téma popisuje, jak připojit experiment ve službě třetí strany k Dynamics 365 Commerce a jak upravovat varianty experimentu.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930158"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Připojení experimentu a úpravy variant

Toto téma popisuje, jak můžete připojit experiment v Commerce a jak můžete provádět změny variant tak, aby odpovídaly vaší hypotéze. Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných tématech.

[ ![Cesta uživatele experimentováním – připojení a úpravy](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Po [nastavení experimentu](experimentation-setup.md) ve službě třetí strany připojíte experiment v Dynamics 365 Commerce a upravíte varianty experimentu.

## <a name="planning-considerations"></a>Poznámky k plánování

Před připojením experimentu v Commerce budete muset udělat několik rozhodnutí, která ovlivní způsob, jakým bude Commerce spravovat váš obsah.

### <a name="determine-the-scope-of-your-experiment"></a>Určení rozsahu experimentu
Když připojíte experiment, budete vyzváni k definování rozsahu experimentu. Experimenty jsou definovány s **částečným** rozsahem nebo s **úplným** rozsahem.
- Zvolte **částečný** rozsah, pokud chcete experiment provádět na konkrétní části stránky. Pokud vyberete tuto možnost, musíte určit, které moduly jsou v experimentu zahrnuty. Změny provedené v částech výchozí stránky nebo fragmentu, které nesouvisí s experimentem, se automaticky synchronizují ve všech variantách.
- Zvolte **úplný** rozsah, pokud chcete experiment provádět na celé stránce nebo v celém fragmentu. Budou vytvořeny samostatné kopie výchozí stránky nebo fragmentu. Nebudete muset vybírat, které moduly jsou v experimentu zahrnuty, protože je možné měnit celou editační plochu. Podle potřeby můžete přidávat a odstraňovat moduly a měnit jejich pořadí. Pokud jsou však provedeny nějaké změny na výchozí stránce nebo fragmentu, ke kterým je experiment přidružen, musí být tyto změny ručně synchronizovány ve všech variantách.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Pokud experiment přidružíte ke stránce, která používá rozložení, můžete zvolit pouze **úplný** rozsah experimentu.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Rozhodnutí, jestli chcete naplánovat, kdy bude experiment publikován
Pokud chcete naplánovat, kdy bude váš experiment publikován na živém webu, ujistěte se, že obsah, který chcete k experimentu přidružit, je dostupný ve skupině publikování *před* připojením experimentu. 

Další informace o skupinách publikování najdete v tématu [Práce se skupinami publikování](publish-groups.md).


## <a name="connect-your-experiment"></a>Připojení experimentu
Když budete chtít experiment připojit, spustíte průvodce **Připojení experimentu** . Průvodce vás provede kroky potřebnými k připojení experimentu. Po dokončení průvodce je váš experiment připojen a jsou vytvořeny varianty, které je možné upravovat.

1. Průvodce spustíte tak, že vyberete kartu **Experimenty** v konfigurátoru webů a pak vyberete **Připojit** . Případně se k průvodci můžete dostat z editoru stránky nebo fragmentů. V režimu úprav vyberte **Připojit experiment** na panelu příkazů.

> [!NOTE]
> Stránka může být připojená vždy jen k jednomu experimentu. Když budete chtít stránku připojit k jinému experimentu, nejprve odstraňte experiment, ke kterému je stránka aktuálně připojená.

1. Zvolte stránku nebo fragment, pro které chcete experiment spustit.
1. Nastavte rozsah experimentování na **částečný** nebo **úplný** na základě toho, co jste zvolili v části [Určení rozsahu experimentu](#determine-the-scope-of-your-experiment) výše.
    > [!NOTE]
    > Příznak funkce **Experimentovat na stránkách nebo ve fragmentech** musí být povolen, pokud chcete experimentovat na celé stránce nebo v celém fragmentu. Další informace najdete v tématu [Experimentování Dynamics 365 Commerce](experimentation-overview.md).
    
1. V posledním kroku průvodce vyberte **Vygenerovat varianty a ukončit průvodce** . Pro experiment se vytvoří varianty. 

## <a name="edit-your-variations"></a>Úpravy variant
Po ukončení průvodce se automaticky vytvoří varianty. 

Pak můžete varianty upravovat tak, aby odrážely možnosti, které potřebujete ověřit v hypotéze experimentu. Vyberte jeden z následujících postupů, který odpovídá rozsahu, který jste pro svůj experiment vybrali v části [Určení rozsahu experimentu](#determine-the-scope-of-your-experiment) výše.

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Úprava variant experimentů s částečným rozsahem
Podle těchto kroků postupujte, pokud jste rozsah experimentu definovali jako **částečný** v průvodci **Připojení experimentu** .

1. V zobrazení editoru použijte rozevírací nabídku variant pod panelem příkazů a upravte každou variantu podle vaší původní hypotézy. Můžete také vytvořit kontrolní nebo základní variantu tak, že jednu z variant ponecháte beze změny.
1. Vyberte modul, u kterého má být experiment spuštěn, vyberte tři tečky (...) a pak vyberte **Přidat do experimentu** .

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Úprava variant experimentů s úplným rozsahem
Pokud jste rozsah experimentu definovali jako **úplný** v průvodci **Připojení experimentu** , pak v zobrazení editoru použijte rozevírací nabídku variant pod panelem příkazů a upravte každou variantu podle vaší původní hypotézy. 

> [!NOTE]
> V obou případech můžete také vytvořit kontrolní nebo základní variantu tak, že jednu z variant ponecháte beze změny.

## <a name="previous-step"></a>Předchozí krok
[Nastavení experimentu](experimentation-setup.md) 


## <a name="next-step"></a>Další krok
[Náhled a publikování experimentu](experimentation-preview-publish.md)
