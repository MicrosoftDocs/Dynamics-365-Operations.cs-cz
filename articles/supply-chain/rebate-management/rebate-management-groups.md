---
title: Skupiny správy rabatu
description: Tento článek popisuje, jak nastavit data pro skupiny správy rabatu. Skupiny správy rabatu lze použít při výpočtech rabatu a lze je připojit k hlavnímu záznamu.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2b948e994783d6ec6f00b77d12bd2594a29f6512
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851529"
---
# <a name="rebate-management-groups"></a>Skupiny správy rabatu

[!include [banner](../includes/banner.md)]

Výpočty správy rabatů mohou být řízeny skupinami. Pro zákazníky, dodavatele a položky lze vytvořit skupiny správy rabatů. Mohou být připojeny k hlavnímu záznamu.

## <a name="rebate-management-customer-groups"></a>Skupiny zákazníka správy rabatu

Výpočet pro skupinu zákazníků se často vytváří pro řetězec společností, jako je řetězec supermarketů nebo franšízová společnost. Tento typ výpočtu obvykle souvisí s rabatem.

Odpočet se často počítá bez ohledu na to, komu byla kvalifikovaná objednávka prodána. Existuje však několik výjimek. Nabyvatel licence může například vytvořit schéma odpočtu, kde skupina zákazníků A obdrží 4 procenta, ale skupina zákazníků B obdrží pouze 3 procenta.

### <a name="set-up-customer-groups"></a>Nastavit skupiny odběratelů

Chcete-li pracovat se skupinami zákazníků správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny zákazníků**. Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny. U každé skupiny je třeba nastavit tato pole:

- **Skupina správy rabatů** – Zadejte jedinečný název skupiny.
- **Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.

### <a name="manage-customer-group-assignments"></a>Správa přiřazení skupin zákazníků

Každý zákazník může patřit do libovolného počtu skupin správy rabatů. Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu zákazníků.

Chcete-li zobrazit, přidat nebo odebrat zákazníky pro vybranou skupinu, postupujte takto.

1. Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny zákazníků**.
1. Vyberte skupinu, kterou chcete spravovat.
1. V podokně akcí vyberte **Zákazníci**. Zobrazí se stránka **Skupiny správy rabatů** se seznamem zákazníků, kteří jsou již členy vybrané skupiny.
1. Chcete-li do skupiny přidat nového zákazníka, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Účet zákazníka** - Vyberte ID účtu zákazníka.

1. Chcete-li odebrat zákazníka ze skupiny, vyberte zákazníka a poté vyberte **Odstranit** v podokně akcí.

Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybraného zákazníka, postupujte takto.

1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. Vyberte zákazníka, se kterým chcete pracovat.
1. V podokně akcí na kartě **Zákazník** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**. Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraný zákazník patří.
1. Chcete-li do nové skupiny přidat zákazníka, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat zákazníka.

1. Chcete-li odebrat zákazníka ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.

## <a name="rebate-management-vendor-groups"></a>Skupiny dodavatelů správy rabatů

Výpočet pro skupinu dodavatelů se často vytváří pro skupinu míst dodání. Tento typ výpočtu obvykle souvisí s rabatem.

### <a name="set-up-vendor-groups"></a>Nastavení skupin dodavatele

Chcete-li pracovat se skupinami dodavatelů správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny dodavatelů**. Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny. U každé skupiny je třeba nastavit tato pole:

- **Skupina správy rabatů** – Zadejte jedinečný název skupiny.
- **Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.

### <a name="manage-vendor-group-assignments"></a>Správa přiřazení skupin dodavatelů

Každý dodavatel může patřit do libovolného počtu skupin správy rabatů. Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu dodavatelů.

Chcete-li zobrazit, přidat nebo odebrat dodavatele pro vybranou skupinu, postupujte takto.

1. Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny dodavatelů**.
1. Vyberte skupinu, kterou chcete spravovat.
1. V podokně akcí vyberte možnost **Dodavatelé**. Zobrazí se stránka **Skupiny správy rabatů** se seznamem dodavatelů, kteří jsou již členy vybrané skupiny.
1. Chcete-li do skupiny přidat nového dodavatele, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Účet dodavatele** - Vyberte ID účtu dodavatele.

1. Chcete-li odebrat dodavatele ze skupiny, vyberte dodavatele a poté vyberte **Odstranit** v podokně akcí.

Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybraného dodavatele, postupujte takto.

1. Přejděte do části **Pohledávky \> Dodavatelé \> Všichni dodavatelé**.
1. Vyberte dodavatele, se kterým chcete pracovat.
1. V podokně akcí na kartě **Dodavatel** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**. Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraný dodavatel patří.
1. Chcete-li do nové skupiny přidat dodavatele, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat dodavatele.

1. Chcete-li odebrat dodavatele ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.

## <a name="item-rebate-groups"></a>Skupiny rabatu pro položky

Seskupením položek získáte větší flexibilitu při výpočtu rabatů a odpočtů. Tento přístup je často efektivnějším způsobem, jak nastavit rabaty a odpočty pro zákazníky a dodavatele.

### <a name="set-up-item-groups"></a>Nastavit skupiny položek

Chcete-li pracovat se skupinami položek správy rabatů, přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**. Můžete použít tlačítka na panelu akcí a podle potřeby přidat a odebrat skupiny. U každé skupiny je třeba nastavit tato pole:

- **Skupina správy rabatů** – Zadejte jedinečný název skupiny.
- **Popis** - Zadejte popis skupiny a poskytněte další informace o tom, jak by měla být použita.

### <a name="manage-item-group-assignments"></a>Správa přiřazení skupin položek

Každá položka může patřit do libovolného počtu skupin správy rabatů. Chcete-li zobrazit a přiřadit členy skupiny, můžete začít buď ze seznamu skupin, nebo ze seznamu položek. Můžete také přidat položky na základě vaší hierarchie kategorií.

Chcete-li zobrazit, přidat nebo odebrat položky pro vybranou skupinu, postupujte takto.

1. Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**.
1. Vyberte skupinu, kterou chcete spravovat.
1. V podokně akcí zvolte **Položky**. Zobrazí se stránka **Skupiny správy rabatů** se seznamem položek, kteří jsou již členy vybrané skupiny.
1. Chcete-li do skupiny přidat novou položku, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Účet položky** - Vyberte ID účtu položky.

1. Chcete-li odebrat položku ze skupiny, vyberte položku a poté vyberte **Odstranit** v podokně akcí.

Chcete-li zobrazit, přidat nebo odebrat přiřazení ke skupině pro vybranéou položku, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte položku, se kterou chcete pracovat.
1. V podokně akcí na kartě **Produkt** ve skupině **Správa rabatů** vyberte **Skupiny správy rabatů**. Zobrazí se stránka **Skupiny správy rabatů** se seznamem skupin, do kterých již vybraná položka patří.
1. Chcete-li do nové skupiny přidat položku, vyberte **Nový** v podokně akcí a přidejte řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Skupina správy rabatů** - Vyberte skupinu, do které chcete přidat položku.

1. Chcete-li odebrat položku ze skupiny, vyberte skupinu a poté vyberte **Odstranit** v podokně akcí.

Chcete-li přidat položky do skupiny na základě vaší hierarchie kategorií, postupujte takto.

1. Přejděte na **Správa rabatů \> Nastavení skupin správy rabatů \> Skupiny položek**.
1. Vyberte skupinu, kterou chcete spravovat.
1. V podokně akcí zvolte **Přidat položky**.
1. V dialogovém okně **Přidat položky** v poli **Hierarchie kategorií** vyberte kategorii nejvyšší úrovně.
1. V levém podokně se otevře hierarchie položek. Vyberte úroveň hierarchie, kterou hledáte. 
1. Položky z vybrané hierarchie a úrovně hierarchie jsou nyní uvedeny v pravém podokně. Při práci s podoknem postupujte takto:

    - Zaškrtněte políčko pro každou položku, kterou chcete přidat.
    - Zaškrtnutím políčka v záhlaví mřížky vyberte všechny uvedené položky.
    - Vyberte tlačítko **Zobrazit vybrané** pro filtrování mřížky tak, aby zobrazovala pouze položky, které jste dosud vybrali. Opětovným stisknutím tlačítka se vrátíte na úplný seznam.

1. Vyberte **OK** a použijte výběr položek na vybranou skupinu.
