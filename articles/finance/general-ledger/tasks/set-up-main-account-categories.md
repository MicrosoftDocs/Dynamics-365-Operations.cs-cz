---
title: Nastavení kategorií hlavního účtu
description: Toto téma vysvětluje, jak nastavit kategorie hlavního účtu v aplikaci Dynamics 365 Finance.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2dcaa27f20ca050d278aa378e90946b8cb40449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815109"
---
# <a name="set-up-main-account-categories"></a>Nastavení kategorií hlavního účtu

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nastavit kategorie hlavního účtu. Kategorie hlavního účtu se používají pro výchozí sestavy ve finančních výkazech a Power BI. Kategorie hlavního účtu, které jsou vytvořeny ve výchozím nastavení, lze přejmenovat, ale nelze je odstranit. Kategorie dalších účtů lze vytvořit a používat pro účely vytváření sestav a analýzy. Toto téma využívá ukázkovou společnost USMF.

## <a name="create-a-main-account-category"></a>Vytvoření kategorie hlavního účtu
1. V navigačním podokně přejděte do části **Moduly >Hlavní kniha > Účtová osnova > Účty > Kategorie hlavního účtu**.
2. Zvolte **Nové**.
3. Do pole **Kategorie hlavního účtu** zadejte jedinečný název.
4. Do pole **Popis** zadejte popis nové kategorie hlavního účtu.
5. V poli **Typ hlavního účtu** vyberte typ hlavního účtu, který bude propojen do kategorie.

## <a name="link-main-accounts-to-account-category"></a>Propojení kategorie účtu s hlavními účty
1. Klikněte na **Připojit hlavní účty**.
2. V seznamu vyberte hlavní účty, které chcete přiřadit do kategorie hlavního účtu zaškrtnutím políček ve sloupci **Propojeno**. Přiřazením hlavních účtů do kategorie hlavních účtů budou nahromaděny zůstatky účtů, když tato kategorie se používá k vytváření finančních sestav a analýzy.  
3. Hlavní účty vyberete zvolením nebo zrušením výběru **Propojeno**.
4. Vyberte **OK**.
5. Vyberte **Ano**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]