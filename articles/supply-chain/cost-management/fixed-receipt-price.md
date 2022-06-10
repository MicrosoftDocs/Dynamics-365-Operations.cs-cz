---
title: Pevná cena příjmu
description: Toto téma vysvětluje, jak můžete nakonfigurovat a používat pevné ceny příjmu v Microsoft Dynamics 365 Supply Chain Management.
author: raprofit
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 8e26d84ddc309249d8bd6e54987ad3ae8eed68f0
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770294"
---
# <a name="fixed-receipt-price"></a>Pevná cena příjmu

[!include [banner](../includes/banner.md)]

**Pevná cena příjmu** je možnost, kterou můžete vybrat ve skupině modelů položek, když používáte jiný model zásob než *Standardní cena* nebo *Klouzavý vážený průměr*. V raných verzích Microsoft Dynamics AX byla tato možnost pojmenována **Standardní cena**. Byla přejmenována na **Pevná cena příjmu**, když byl v Dynamics AX 2012 představen nový model standardních nákladů. Toto téma vysvětluje, jak můžete nakonfigurovat a používat pevné ceny příjmu v Dynamics 365 Supply Chain Management.

## <a name="about-fixed-receipt-prices"></a>Informace o Pevných cenách příjmu

Když vyberete zaškrtávací políčko **Pevná cena příjmu** na stránce **Skupina modelů položek** pro položku, systém použije cenu příjmu jako standardní cenu pro příjem zásob. Pokud se nákupní cena a výchozí nákladová cena položky, která je nakonfigurována pro produkt, liší, rozdíl se zaúčtuje na účet **Pevná cena příjmu - zisk** nebo **Pevná cen příjmu - ztráta** a na protiúčet účtu **Fixní cena příjmu - protiúčet**, který zadáte na stránce **Profil účtování zásob**.

Protože se možnost **Pevná cena příjmu** používá ve spojení s různými modely zásob (jako je první do skladu, první ven (FIFO), poslední do skladu, první ven (LIFO) a vážený průměr), proces *Závěrka a úprava zásob* bude stále vytvářet vyrovnání a opravné položky podle principu inventarizace, který vyberete na stránce **Skupina modelů položek**. Úpravy se však provádějí pouze u výdejů ze zásob.

Například jste nakonfigurovali produkt se skupinou modelů položek, kde je pole **Model zásob** nastaveno na *FIFO* a je vybrána možnost **Pevná cena příjmu**. Když obdržíte zásoby prostřednictvím nákupní objednávky, hodnota zásob se nastaví na hodnotu výchozí nákladové ceny položky v době příjmu produktu. Když fakturujete nákupní objednávku, pokud je fakturovaná cena odlišná, systém zaúčtuje výchozí nákladovou cenu uvolněného produktu na účet zásob. Rozdíl zaúčtuje na účet Fixní cena příjmu - zisk nebo Fixní cena přijmu - ztráta. Později, když produkt prodáte nebo spotřebujete, systém použije průběžný průměr pro položku v době, kdy byla faktura prodejní objednávky zaúčtována (pokud nepoužijete označení).

Pokud použijete proces *Závěrka a úprava zásob*, systém vytvoří vyrovnání s prvním výdejem proti prvnímu příjmu. Rozdíl mezi cenou příjmu, která byla použita v příjmu, a průběžným průměrem, který byl použit na výdeji, je zaúčtován v novém poukazu.

## <a name="enable-fixed-receipt-prices"></a>Povolit Pevné ceny příjmu

Chcete-li povolit pevné ceny příjmu pro položku, postupujte takto.

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Zásoby \> Skupiny modelu položky**.
2. Vytvořte novou modelovou skupinu položek nebo vyberte existující modelovou skupinu.
3. Na pevné záložce **Metoda kalkulace a účtování nákladů** vyberte zaškrtávací políčko **Pevná cena příjmu**.

    > [!NOTE]
    > Nemůžete vybrat zaškrtávací políčko **Pevná cena příjmu**, pokud je pole **Model zásob** nastaveno na *Standardní cena* nebo *Klouzavý průměr*.

4. Zavřete stránku.

Poté, co povolíte možnost **Pevná cena příjmu**, musíte aktualizovat svůj profil účtování zásob podle následujících kroků.

1. Přejděte na **Řízení zásob \> Nastavit \> Zaúčtování \> Zaúčtování**.
1. Na kartě **Nákupní objednávka** ve sloupci **Výběr** vyberte **Pevná cena příjmu - zisk**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Nastavte nový řádek tak, aby se vztahoval na modelovou skupinu položek, pro kterou jste povolili pevné oceňování příjmu, a určete hlavní účet, který se používá k zaúčtování zisků z pevných cen příjmu pro nákupní objednávky. Nakonfigurujte další nastavení podle potřeby.
1. Ve sloupci **Výběr** vyberte **Pevná cena příjmu - ztráta**. Přidejte nový řádek tak, aby se vztahoval na modelovou skupinu položek, pro kterou jste povolili pevné oceňování příjmu, a určete hlavní účet, který se používá k zaúčtování ztrát z pevných cen příjmu pro nákupní objednávky. Nakonfigurujte další nastavení podle potřeby.
1. Ve sloupci **Výběr** vyberte **Pevná cena příjmu - protiúčet**. Přidejte nový řádek tak, aby se vztahoval na modelovou skupinu položek, pro kterou jste povolili pevné oceňování příjmu, a určete hlavní účet, který se používá k zaúčtování protiúčtu z pevných cen příjmu pro nákupní objednávky. Nakonfigurujte další nastavení podle potřeby.
1. Na kartě **Zásoby** ve sloupci **Výběr** vyberte **Pevná cena příjmu - zisk**. Přidejte nový řádek tak, aby se vztahoval na modelovou skupinu položek, pro kterou jste povolili pevné oceňování příjmu, a určete hlavní účet, který se používá k zaúčtování zisku ze pevných cen příjmu pro zásoby. Nakonfigurujte další nastavení podle potřeby.
1. Ve sloupci **Výběr** vyberte **Pevná cena příjmu - ztráta**. Přidejte nový řádek tak, aby se vztahoval na modelovou skupinu položek, pro kterou jste povolili pevné oceňování příjmu, a určete hlavní účet, který se používá k účtování ztrát ze pevných cen příjmu pro zásoby. Nakonfigurujte další nastavení podle potřeby.

> [!NOTE]
> Obvykle doporučujeme, aby pole **Pevná cena příjmu - zisk** a **Pevná cena příjmu - ztráta** používaly stejný hlavní účet pro nákupní objednávky i zásoby.

> [!IMPORTANT]
> Když změníte hodnotu v poli **Cena** pole na pevné záložce **Správa nákladů** na stránce **Uvolněné produkty**, systém automaticky nepřeceňuje zásoby, které jsou k dispozici. Jako ruční řešení otevřete stránku **Závěrka a vyrovnání** a vyberte **Vyrovnání \> Na skladě** v podokně akcí. Poté vyberte položky, které jsou na skladě, a upravte je na aktuální cenu. Jednou jasnou výhodou použití standardního nákladového modelu zásob je to, že způsobí, že systém automaticky přecení zásoby na skladě.
