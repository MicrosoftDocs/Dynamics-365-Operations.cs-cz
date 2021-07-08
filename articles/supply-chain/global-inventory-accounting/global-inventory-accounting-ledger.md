---
title: Hlavní kniha globálního účetnictví zásob
description: Toto téma popisuje účetní knihy Globálního účetnictví zásob, které jsou definovány kombinací měny, kalendáře, konvence a přidružení k právnické osobě.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273124"
---
# <a name="global-inventory-accounting-ledger"></a>Hlavní kniha globálního účetnictví zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Globální účetnictví zásob má vlastní sadu účetních knih. Pokaždé, když je pro příslušnou právnickou osobu zpracována transakce související se zásobami, může systém podle potřeby tuto transakci zaúčtovat do libovolného počtu účetních knih globálního účetnictví zásob.

Hlavní kniha je registr opatření na straně má dáti a dal. Tato opatření jsou klasifikována pomocí nákladových položek a účtů podřízené knihy. Hlavní kniha Globálního účetnictví zásob je definována kombinací měny, kalendáře, konvence a přidružení k právnické osobě.

Chcete-li nastavit své účetní knihy globálního účetnictví zásob, přejděte na **Globální účetnictví zásob \> Založit \> Účetní knihy globálního účetnictví zásob**. U každé účetní knihy je třeba nastavit tato pole:

- **Název** – Zadejte název účetní knihy.
- **Popis** - zadejte popis účetní knihy.
- **Fiskální kalendář** - Určete fiskální kalendář pro hlavní knihu.
- **Typ měny a směnného kurzu** - Pomocí polí na této pevné záložce vyberte účetní měnu, kterou účetní kniha používá, a typ směnného kurzu. Měna, kterou vyberete, se může lišit od měny, kterou právnická osoba používá. V globálním účetnictví zásob mohou uživatelé definovat tolik účetních knih pro výpočet nákladů, kolik požadují. Globální účetnictví zásob podporuje účtování zásob ve více měnách a ve více oceněních. Nastavte následující pole:

    - **Měna** - Vyberte měnu výpočtu nákladů, ve které jsou udržovány hodnoty související se zásobami. Mezi tyto hodnoty patří hodnota zásob, náklady na prodané zboží, zásoby na cestě a všechny druhy odchylek.
    - **Typ směnného kurzu** - Vyberte směnný kurz, který by měl systém použít k převodu částky transakce v měně transakce a standardních nákladů na položky do měny kalkulace.

- **Název konvence** - Upřesněte konvenci. Konvence je kolekcí zásad, které určují, jak budou náklady účtovány v této účetní knize.
- **Právnická osoba** - Hlavní kniha bude účtovat dokumenty, které jsou zaúčtovány vybrané právnické osobě.
- **Plnění** - Vyberte, zda mají být transakce zásob, které byly vytvořeny před vytvořením hlavní knihy, zpracovány podle měny a konvence v hlavní knize. Vyberte jednu z následujících hodnot:

    - **Aktivováno** - Hlavní kniha by měla zpracovat transakce, které byly vytvořeny před vytvořením hlavní knihy.
    - **Deaktivováno** - Hlavní kniha by měla zpracovat pouze transakce, které jsou vytvořeny po vytvoření hlavní knihy.

    > [!IMPORTANT]
    > **Nebudete** moci se vrátit a nastavit toto pole po zadání nových dokumentů.

- **Stav** - Systém automaticky nastaví stav nově vytvořených knih na *Připravit*.
