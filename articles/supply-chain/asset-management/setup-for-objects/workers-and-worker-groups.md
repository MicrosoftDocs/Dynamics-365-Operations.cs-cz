---
title: Pracovníci údržby a skupiny pracovníků
description: Tento článek vysvětluje, jak nastavit pracovníky údržby skupiny pracovníků v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a24c880ee76af1490824aef07976b998d9225d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860892"
---
# <a name="maintenance-workers-and-worker-groups"></a>Pracovníci údržby a skupiny pracovníků

[!include [banner](../../includes/banner.md)]

 

Tento článek vysvětluje, jak nastavit pracovníky údržby skupiny pracovníků v modulu Správa majetku. V modulu Správa majetku můžete pracovníky údržby připojit k funkčním místům. (Další informace o funkčních umístěních naleznete v tématu [Tvorba funkčních míst](../functional-locations/create-functional-locations.md).) Tato funkce může být užitečná například v případě, že plánujete úlohu údržby stroje, který je umístěn na funkčním místě 01, a chcete práci přidělit pracovníkům údržby ze stejného místa.

Můžete také vytvořit skupiny pracovníků údržby a přidružit k nim pracovníky údržby. Tato funkce je užitečná, když provádíte jednoduché plánování pracovních zakázek a chcete naplánovat skupinu údržbářských pracovníků na pracovní příkaz. Pracovníky údržby a údržbářské skupiny můžete použít k nastavení preferovaných pracovníků údržby a zodpovědných pracovníků údržby. 


## <a name="create-workers"></a>Vytvořit pracovníky

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovníci** \> **Pracovníci**.
2. Vyberte **Nový** pro přidání pracovníka na seznam.
3. V poli **Pracovník** vyberte pracovníka.
4. Nastavením možnosti **Aktivní** na **Ano** naplánujete pracovníka na pracovní příkazy.

    Na pevné záložce **Obecné** jsou pole **Prostředek** a **Popis** automaticky vyplněna, pokud byl zdroj vybrán pro pracovníka. Pole **Kalendář** je také vyplněno automaticky, pokud jste pracovníka nastavili jako zdroj a přidělili k danému zdroji kalendář na stránce **Prostředky** (**Správa organizace** \> **Prostředky** \> **Prostředky**).

5. Na pevné záložce **Skupiny** vyberte **Přidat** a pak vyberte skupinu pracovníků údržby pro pracovníka. Pracovník může být přiřazen k více než jedné skupině.
6. Ve standardním nastavení je příslušnost pracovníka ke skupině účinná od data přidání skupiny a nikdy nevyprší. Toto datum je zobrazeno v poli **Účinnost**. Chcete-li zobrazit pole **Účinnost** vyberte **Zobrazit** \> **Vše**. Pokud má být přidružení pracovníka ke skupině omezeno na určité období, definujte období pomocí **Účinnost** a **Vypršení platnosti**.
7. Na pevné záložce **Funkční místa** vyberte **Přidat** a pak vyberte funkční místo pro pracovníka údržby. Zadejte také, které místo je primárním funkčním místem pracovníka.

    > [!NOTE]
    > Po přidání funkčních umístění pracovníkovi se veškerý aktivní majetek, který se vztahuje k těmto funkčním místům, zobrazí v různých položkách nabídky, jako je například **Můj aktivní majetek** a **Moje aktivní funkční místa**. Zobrazí se také ve vyhledávání majetku, které se zobrazí při vytvoření nového majetku, požadavku na údržbu nebo pracovního příkazu.

    Pole na pevné záložce **Podrobnosti** zobrazí počet skupin údržby a funkčních míst, ke kterým se vybraný pracovník údržby vztahuje.

## <a name="create-worker-groups"></a>Vytvořit skupiny pracovníků

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovníci** \> **Skupiny pracovníků údržby**.
2. Vyberte **Nový** pro přidání skupiny pracovníků na seznam.
3. Do pole **Skupina pracovníků údržby** zadejte ID skupiny.
4. Do pole **Název** zadejte název.
5. Na pevné záložce **Pracovníci** vyberte **Přidat** a pak vyberte skupinu pracovníků údržby pro skupinu pracovníků. Informace o polích **Účinnost** a **Vypršení platnosti** najdete v kroku 6 v předchozí proceduře.
6. Pokud má skupina prostředků souviset s vybranou skupinou údržbářských pracovníků, vyberte možnost **Kopírovat ze skupiny prostředků**. V poli **Skupina** vyberte skupinu zdrojů, ze které chcete kopírovat nastavení kalendáře. Potom v poli **Skupina pracovníků** vyberte skupinu pracovníků, ke které chcete zkopírovat nastavení kalendáře skupiny prostředků. Tento krok je relevantní pouze v případě, že chcete, aby pracovníci údržby používali kalendář, který se vztahuje k prostředku (pracovnímu středisku) během plánování pracovního příkazu.

    Pole na pevné záložce **Podrobnosti** zobrazí počet pracovníků údržby a funkčních míst, které byly vytvořeny ve zvolené skupině pracovníků údržby.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]