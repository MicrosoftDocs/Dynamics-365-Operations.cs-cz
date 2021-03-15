---
title: Vytvoření výchozího odběratele
description: V tomto tématu je popsán postup při vytvoření výchozího odběratele, který se použije při vytváření kanálu v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1dd4dfc5b8ca7af66941d081b4c20be0f5d6001d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993393"
---
# <a name="create-a-default-customer"></a>Vytvoření výchozího odběratele


[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při vytvoření výchozího odběratele, který se použije při vytváření kanálu v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Při vytváření kanálu budete muset zadat výchozího odběratele. Po prvním vytvoření skupiny odběratelů a adresáře odběratelů lze snadno vytvořit výchozího odběratele.

## <a name="create-a-customer-group"></a>Vytvoření skupiny odběratelů

Pokud žádné skupiny odběratelů dosud neexistují, můžete je vytvořit. Příklady mohou být skupiny, které představují různé skupiny odběratelů (například velkoobchod, maloobchod, Internet, zaměstnanci atd.).

Pokud chcete vytvořit skupinu odběratelů, postupujte takto.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Zákazníci \> Skupiny zákazníků**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Skupina zákazníků** zadejte ID skupiny.
1. Je-li to nutné, zadejte popis do pole **Popis**.
1. Do pole **Podmínky plateb** zadejte příslušnou hodnotu.
1. Do pole **Čas mezi datem splatnosti a datem platby** zadejte odpovídající hodnotu.
1. Do pole **výchozí daňová skupina** zadejte, pokud je to vhodné, daňovou skupinu.
1. Zaškrtněte políčko **Ceny zahrnují DPH** v připadě potřeby.
1. Do pole **výchozí důvod odpisu** zadejte odpovídající hodnotu v připadě potřeby.

Následující obrázek znázorňuje několik konfigurovaných skupin odběratelů.

![Skupiny odběratelů](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Vytvoření adresáře odběratelů

Zákazník musí být přidružen k adresáři. Pokud ještě nebyla vytvořena, je třeba ji vytvořit.

Při vytváření nového adresáře odběratelů postupujte takto:

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Adresáře**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název** zadejte název.
1. Zadejte popis do pole **Popis**.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad adreáře.

![Adresář](media/address-book.png)

## <a name="create-a-default-customer"></a>Vytvoření výchozího odběratele

Pokud chcete vytvořit výchozího odběratele, postupujte takto.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Zákazníci \> Všichni odběratelé**.
1. V podokně akcí zvolte **Nový**.
1. V rozevíracím seznamu **Typ** vyberte "Osoba".
1. V rozevíracím seznamu **účet odběratele** vyberte nebo zadejte číslo účtu (například "100001").
1. V rozevíracím seznamu **Křestní jméno** vyberte nebo zadejte název (například "výchozí").
1. V rozevíracím seznamu **Prostřední jméno** vyberte nebo zadejte název (například "Retail").
1. V rozevíracím seznamu **Příjmení** vyberte nebo zadejte název (například "Zákazník").
1. V rozevíracím seznamu **Měna** vyberte nebo zadejte měnu (například "USD").
1. V rozevíracím seznamu **Měna** vyberte skupinu odběratelů, která byla vytvořena dříve.
1. V rozevíracím seznamu **Adresáře** vyberte existující adresář odběratele.
1. Výběrem **Uložit** uložte a vrátíte se do obrazovky s podrobnostmi o odběrateli pro nového odběratele.

> [!NOTE]
> Není nutné přidávat adresu výchozího odběratele.

Na následujícím obrázku je znázorněn příklad vytvoření zákazníka.

![Vytvoření výchozího odběratele](media/default-customer-creation.png)

Následující obrázek znázorňuje výchozí konfiguraci odběratele.

![Konfigurace ukázkového odběratele](media/default-customer-configuration1.png)

Většina výchozích hodnot na obrazovce podrobností odběratele může zůstat, ale je třeba změnit dvě hodnoty.

1. Na obrazovce Podrobnosti o odběrateli rozbalte **Výhozí nastavení prodejní objednávky**.
1. V rozevíracím seznamu **Umístění** vyberte nebo zadejte přednastavené umístění.
1. V rozevíracím seznamu **Sklad** vyberte nebo zadejte přednastavený sklad.

Na následujícím obrázku je znázorněn příklad konfigurace zákazníka.

![Konfigurace ukázkového odběratele](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Další zdroje

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]