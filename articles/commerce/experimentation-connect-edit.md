---
title: Připojení experimentu a úpravy variant
description: Tento článek popisuje, jak připojit experiment ve službě třetí strany k Dynamics 365 Commerce a jak upravovat varianty experimentu.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942815"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Připojení experimentu a úpravy variant

Tento článek popisuje, jak můžete připojit experiment v Commerce a jak můžete provádět změny variant tak, aby odpovídaly vaší hypotéze. 

Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných článcích.

[ ![Cesta uživatele experimentováním – připojení a úpravy.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Po [nastavení experimentu](experimentation-setup.md) ve službě třetí strany připojíte experiment v Dynamics 365 Commerce a upravíte varianty experimentu.

## <a name="connect-your-experiment"></a>Připojení experimentu
Když budete chtít experiment připojit, spustíte průvodce **Připojení experimentu**. Průvodce vás provede kroky potřebnými k připojení experimentu. Po dokončení průvodce je váš experiment připojen a jsou vytvořeny varianty, které je možné upravovat.

Chcete-li zahájit připojení experimentu v nástroji pro tvorbu obchodních webů, postupujte takto.

1. Chcete-li spustit průvodce **Připojte experiment**, vyberte **Experimenty** v levém navigačním podokně a poté vyberte **Připojit**. Alternativně můžete průvodce otevřít ze editoru stránky nebo fragmentu jeho úpravou a výběrem **Připojte experiment** na panelu příkazů.

    > [!NOTE]
    > - Stránka může být připojená vždy jen k jednomu experimentu. Když budete chtít stránku připojit k jinému experimentu, nejprve odstraňte experiment, ke kterému je stránka aktuálně připojená.
    > - Experimentovat můžete pouze na stránkách s vlastním rozložením. Pokud má vaše stránka přednastavené rozložení, nejprve jej převeďte na vlastní rozložení. Můžete to udělat tak, že přejdete na stránku a vyberete **Převést na vlastní rozložení** na příkazovém řádku. Další informace o rozloženích viz [Přednastavená a vlastní rozložení](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Pokud se připojujete k experimentu z karty **Experimenty** v levém navigačním panelu, vyberte název experimentu ze seznamu, který se zobrazí.
1. Zvolte stránku nebo fragment, pro které chcete experiment spustit.
1. V posledním kroku průvodce vyberte **Vygenerovat varianty a ukončit průvodce**. Pro experiment se vytvoří varianty. 

> [!NOTE]
> Pokud chcete naplánovat, kdy bude váš experiment publikován na živém webu, ujistěte se, že obsah, který chcete k experimentu přidružit, je dostupný ve skupině publikování *před* připojením experimentu. Další informace o skupinách publikování najdete v tématu [Práce se skupinami publikování](publish-groups.md).

## <a name="edit-your-variations"></a>Úpravy variant

Když opustíte průvodce **Připojit experiment**, jsou pro vás vytvořeny varianty. Následujícím postupem upravíte varianty tak, aby odrážely možnosti, které potřebujete ověřit v hypotéze experimentu.

1. V zobrazení editoru použijte rozevírací nabídku variant pod panelem příkazů a upravte každou variantu podle vaší původní hypotézy. Můžete také vytvořit kontrolní nebo základní variantu tak, že jednu z variant ponecháte beze změny.
1. Vyberte modul, u kterého má být experiment spuštěn, vyberte tři tečky (...) a pak vyberte **Přidat do experimentu**.

> [!NOTE]
> Zvažte vytvoření kontrolní nebo základní varianty tak, že jednu z variant ponecháte beze změny.

## <a name="previous-step"></a>Předchozí krok
[Nastavení experimentu](experimentation-setup.md) 


## <a name="next-step"></a>Další krok
[Náhled a publikování experimentu](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
