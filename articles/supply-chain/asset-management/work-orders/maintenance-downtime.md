---
title: Prostoj údržby
description: Tohle téma popisuje prostoje údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918237"
---
# <a name="maintenance-downtime"></a>Prostoj údržby


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Registrace prostojů údržby můžete vytvořit u majetku vybraného v pracovním příkazu. To je užitečné v případě, že chcete zaznamenávat prostoje údržby na jednom nebo více počítačích v produkční oblasti. Nejprve vytvořte kódy důvodů prostojů údržby, které chcete použít, například porucha nebo plánované zastavení. To se provádí v části **Kódy důvodů prostojů údržby**. Dále můžete vytvořit registrace prostojů údržby v části **Prostoje údržby** a přidat odpovídající kódy důvodů.

## <a name="create-maintenance-downtime-reason-codes"></a>Vytváření kódů důvodů prostojů údržby

1. Klikněte na položky **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Kódy důvodů prostojů údržby**.

2. Klepněte na možnost **Nový**.

3. Do pole **Kód důvodu prostoje údržby** zadejte ID.

4. Do pole **Název** zadejte název kódu důvodu.

5. Chcete-li, aby byl kód důvodu zahrnut do výpočtů klíčového indikátoru výkonu, zaškrtněte políčko **Zahrnout do ukazatele KPI**. Obvykle by plánované zastavení výroby nemělo být zahrnuto do výpočtů ukazatelů KPI, protože neovlivňují očekávaný výkon.

6. Klikněte na možnost **Uložit**.

![Obrázek č. 1](media/15-work-orders.png)


Po vytvoření kódů důvodů prostojů údržby, které chcete použít, můžete vytvořit registrace prostojů údržby pro pracovní příkazy a majetek.


## <a name="create-maintenance-downtime-registrations"></a>Vytvoření registrací prostojů údržby

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz a klikněte na položku **Prostoj údržby**.

3. Klepněte na možnost **Nový**.

4. Do polí **Od** a **Do** zadejte interval data a času pro registraci prostoje údržby.

5. Když ponecháte pole **Do** prázdné, do pole **Doba trvání** bude automaticky vložena doba trvání v hodinách.

6. V poli **Kód důvodu prostoje údržby** vyberte kód důvodu.

7. Chcete-li přidat další registrace, zopakujte kroky 3–6.

8. Klikněte na možnost **Uložit**.


![Obrázek č. 2](media/16-work-orders.png)


Kalendář použitý k výpočtu registrace prostoje údržby závisí na výběru v nastavení majetku a parametrů. Pokud je prostředek vybrán pro majetek v umístění **Všechen majetek** >  záložka s náhledem **Dlouhodobý majetek** > pole **Prostředek**, použije se nastavený kalendář pro přidruženou skupinu prostředků, jak je znázorněno na následujícím obrázku.

![Obrázek č. 3](media/17-work-orders.png)


Není-li pro majetek vybrán žádný prostředek, použije se standardní kalendář vybraný v části **Parametry správy majetku**, jak je znázorněno na následujícím obrázku.

![Obrázek č. 4](media/18-work-orders.png)


Kliknutím na položky **Správa podnikového majetku** > **Dotazy** > **Prostoj údržby** zobrazíte přehled všech registrací prostojů údržby.

>[!NOTE]
>Všechny kalendáře používané v modulu **Správa majetku** se nastavují v umístění **Správa organizace** > **Nastavení** > **Kalendáře** > **Kalendáře**.

