---
title: Prostoj údržby pro pracovní příkazy
description: Tohle téma popisuje jak vytvořit registrace prostojů údržby u majetku vybraného v pracovním příkazu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 263a044a0a378e95ea271ac1c6f468f9e3287f26
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423632"
---
# <a name="maintenance-downtime-for-work-orders"></a>Prostoj údržby pro pracovní příkazy

[!include [banner](../../includes/banner.md)]


Registrace prostojů údržby můžete vytvořit u majetku vybraného v pracovním příkazu. Tato schopnost je užitečná v případě, že chcete zaznamenávat prostoje údržby na jednom nebo více počítačích v produkční oblasti. Nejprve vytvořte kódy důvodů prostojů údržby, které chcete použít, například **Rozdělení** a **Plálnované zastavení**. Tento krok se provádí na stránce **Kódy důvodů prostojů údržby**. Dále můžete vytvořit registrace prostojů údržby na stránce **Prostoje údržby** a přidat příslušné kódy důvodů prostoje údržby.

## <a name="create-maintenance-downtime-reason-codes"></a>Vytváření kódů důvodů prostojů údržby

1. Vyberte položky **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Kódy důvodů prostojů údržby**.

2. Zvolte **Nové**.

3. Do pole **Kód důvodu prostojů údržby** zadejte ID pro kód důvodu prostojů údržby.

4. Do pole **Název** zadejte název.

5. Zaškrtněte políčko **Zahrnutí KPI**, pokud by měl být kód důvodu zahrnut do výpočtů klíčových ukazatelů výkonu (KPI) pro majetek. Obecně platí, že by plánované zastavení výroby nemělo být zahrnuto do výpočtů ukazatelů KPI, protože neovlivňují očekávaný výkon.

6. Zvolte **Uložit**.

Následující ilustrace znázorňuje příklad stránky **Kódy důvodu prostoje údržby**.

![Obrázek č. 1](media/15-work-orders.png)

Po vytvoření kódů důvodů prostojů údržby, které chcete použít, můžete vytvořit registrace prostojů údržby pro pracovní příkazy a majetek.


## <a name="create-maintenance-downtime-registrations"></a>Vytvoření registrací prostojů údržby

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz a pak na kartě **Pracovní příkaz** ve skupině **Majetek** vyberte **Prostoj údržby**.

3. Zvolte **Nové**.

4. Do polí **Od** a **Do** zadejte interval data a času pro registraci prostoje údržby.

>[!NOTE]
>Když ponecháte pole **Do** prázdné, do pole **Doba trvání** bude automaticky vložena doba trvání v hodinách.

5. V poli **Kód důvodu prostoje údržby** vyberte kód důvodu.

6. Opakováním kroků 3 až 5 přidejte další registrace.

7. Zvolte **Uložit**.

Následující ilustrace znázorňuje příklad stránky registrace prostoje údržby.

![Obrázek č. 2](media/16-work-orders.png)

Kalendář použitý k výpočtu registrace prostoje údržby závisí na výběru v nastavení majetku a parametrů. Pokud je prostředek vybrán pro majetek v poli **Prostředek** pevné záložky **Investiční majetek** na stránce **Veškerý majetek**, použije se nastavený kalendář pro přidruženou skupinu prostředků, jak je znázorněno na následujícím obrázku.

![Obrázek č. 3](media/17-work-orders.png)

Není-li pro majetek vybrán žádný prostředek, použije se standardní kalendář vybraný v části **Parametry správy majetku**, jak je znázorněno na následujícím obrázku.

![Obrázek č. 4](media/18-work-orders.png)

Pokud chcete zobrazit přehled všech registrací prostojů údržby, klikněte na **Správa majetku** > **Dotazy** > **Prostoj údržby**.

>[!NOTE]
>Všechny kalendáře používané v modulu **Správa majetku** se nastavují v umístění **Správa organizace** > **Nastavení** > **Kalendáře** > **Kalendáře**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]