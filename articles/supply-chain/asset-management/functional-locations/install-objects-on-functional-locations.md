---
title: Instalace majetku na funkčních místech
description: Tento článek vysvětluje, jak nainstalovat majetek na funkční místa v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ae571f4ad7210b31d212b0472610b36dc5c488b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016065"
---
# <a name="install-assets-on-functional-locations"></a>Instalace majetku na funkčních místech

[!include [banner](../../includes/banner.md)]

 

Další krok po vytvoření struktur funkčních míst je instalace majetku do příslušných funkčních míst. Tento článek vysvětluje, jak nainstalovat majetek na tato funkční místa v modulu Správa majetku. Informace o způsobu vytvoření majetku naleznete v tématu [Úvod do modulu Majetek](../objects/introduction-to-objects.md).

Pokud jste vytvořili strukturu majetku, musí být celá struktura majetku nainstalována na funkčním místě. Proto lze na funkčním místě vybrat pouze nadřazený majetek (majetek nejvyšší úrovně, který nemá žádný nadřazený majetek). Všechny související podřízené majetky (dílčí majetky) budou také instalovány do funkčního místa. Při instalaci majetku do funkčního místa mohou být do nich automaticky převedeny finanční dimenze funkčního místa, a to v závislosti na nastavení typu funkčního místa, které je vybráno pro funkční místo. Další informace o nastavení typů funkčního místa naleznete v tématu [Typy funkčního místa](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> U typu funkčního místa, který se používá pro funkční místo, můžete nastavit typy majetku. V takovém případě se při instalaci majetku do funkčního místa zobrazí v seznamu majetku, který lze nainstalovat do funkčního místa, pouze nadřazený majetek, který má stejný typ majetku.

Po nainstalování majetku do funkčního místa můžete podle potřeby nahradit nadřazený majetek nebo strukturu majetku. Jako při instalaci majetku vyberte nadřazený majetek, který chcete nahradit. Bude také nahrazen veškerý související podřízený majetek. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Instalace struktury majetku na funkční místo

1. Zvolte **Správa majetku** \> **Funkční místa** \> **Všechna funkční místa** nebo **Aktivní funkční místa**.
2. Zvolte funkční místo, na které chcete nainstalovat majetek.
3. Vyberte **Instalovat majetek**.

    Oddíl **Atributy** zobrazuje seznam požadavků na atributy majetku nastavených pro typ funkčního místa, který je vybrán pro funkční místo. Atributy jsou určeny pouze pro informaci. Systém neověřuje atributy vůči atributům majetku, které jsou nastaveny u majetku, který instalujete. Toto ověření je nutné provést po vybrání majetku v poli **Majetek**.

4. V poli **Majetek** vyberte nadřazený majetek, který chcete nainstalovat. Do instalace jsou automaticky zahrnuty všechny související podřízené majetky.

    Oddíl **Atributy majetku** vpravo od seznamu majetku zobrazuje atributy majetku, které souvisejí s vybraným majetkem.

5. V poli **Počátek platnosti** vyberte datum a čas, od kterého je daná instalace majetku platná. Po tomto datu a čase budou náklady majetku a související dílčí majetky spojeny s funkčním místem.

    > [!NOTE]
    > Atributy majetku, které jsou nastaveny u majetku, jsou přidány do části **Atributy**. Například požadavek na atribut **Hmotnost** byl přidán jako požadavek na majetek i na funkční místo. Pokud majetek obsahuje požadavky na atributy stejného typu jako funkční místo, budou hodnoty požadavků na atributy majetku zadány do polí **Hodnoty**. Proto můžete ověřit hodnoty majetku podle požadavků na atributy nastavených na funkčním místě. Požadavky na atributy nastavené na funkčním místě jsou označeny zaškrtnutím.

6. Vyberte **OK**.

    > [!NOTE]
    > Chcete-li změnit instalaci majetku tak, že jej nainstalujete do nového funkčního místa, postupujte podle kroků 1 až 6 tohoto postupu. Při instalaci majetku do nového funkčního místa je majetek automaticky odinstalován z předchozího funkčního místa. Všechny aktivní požadavky na údržbu nebo pracovní příkazy, které byly vytvořeny na majetku před jeho instalací do nového funkčního místa, **nejsou** automaticky přeneseny do nového funkčního místa. Pokud jsou tyto požadavky na údržbu a pracovní příkazy pro majetek stále požadovány, je nutné je po instalaci majetku do nového místa ručně znovu vytvořit.

7. Chcete-li zobrazit seznam všech majetků, včetně dílčích majetků, které jsou nainstalovány na funkčním místě, vyberte funkční místo na stránce **Všechna funkční místa** a pak vyberte **Majetek**.
8. Chcete-li zobrazit seznam aktivních požadavků na údržbu, aktivních pracovních příkazů nebo registrací závad, které souvisejí s majetkem nainstalovaným na funkčním místě, vyberte funkční místo na stránce **Všechna funkční místa** a pak vyberte **Požadavky**, **Pracovní příkazy** nebo **Závady**.

> [!NOTE]
> Když se data související s majetkem změní, automaticky se aktualizují ve funkčním místě, na kterém je majetek instalován. Tato automatická aktualizace se týká změn požadavků na údržbu, pracovních příkazů, registrací závad majetku, registrací prostoje údržby a registrací měření majetku.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Automatické vytvoření jednoho majetku na funkčním místě

Pro zpracování automatického vytváření *jednoho* majetku na funkčním místě můžete nastavit fáze funkčních míst a typy funkčních míst. Majetek získá stejné ID a název jako funkční místo. Tato funkce může být užitečná, pokud zpracováváte údržbu velkého statického majetku, jako je například budova.

Než bude možné automaticky vytvořit majetek na funkčním místě, musí být k dispozici následující data nastavení:

- Vytvořte typ funkčního místa pro zpracování automatického vytváření majetku. V poli **Typ majetku** vyberte typ majetku. Další informace naleznete v tématu [Typy funkčních míst](../setup-for-functional-locations/functional-location-types.md).
- Vytvořte stav životního cyklu funkčního místa pro zpracování automatického vytváření majetku. Nastavte možnost **Vytvořit majetek** na **Ano**. Další informace naleznete v tématu [Stavy životního cyklu funkčních míst](../setup-for-functional-locations/functional-location-stages.md).

Jakmile jsou k dispozici data nastavení, jste připraveni k vytvoření majetku.

1. Na stránce **Všechna funkční místa** se ujistěte, že funkční místo, kde chcete majetek automaticky vytvořit, používá typ funkčního místa, který jste pro tento účel vytvořili.
2. V seznamu vyberte funkční místo.
3. Vyberte **Aktualizovat stav funkčního místa** a pak vyberte stav životního cyklu, který jste pro tento účel vytvořili. Jeden majetek je nyní automaticky nainstalován na funkční místo. Tento majetek má stejný název jako funkční místo.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]