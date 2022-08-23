---
title: Kopírování obsahu do jiného národního prostředí
description: Tento článek popisuje, jak zkopírovat existující obsah do jiného národního prostředí v rámci webu v konfigurátoru webů Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269254"
---
# <a name="copy-content-to-another-locale"></a>Kopírování obsahu do jiného národního prostředí

[!include[banner](../includes/banner.md)]

Tento článek popisuje, jak zkopírovat existující obsah do jiného národního prostředí v rámci webu v konfigurátoru webů Microsoft Dynamics 365 Commerce.

Když vytváříte obsah v konfigurátoru webů Commerce, je vždy spojen s identifikátorem národního prostředí, například „en-us“. Jednotlivé stránky a položky můžete zkopírovat do jiného národního prostředí v rámci stejného webu elektronického obchodu přepnutím národního prostředí při úpravě položky obsahu a vytvořením nové varianty položky. V některých případech, například když spouštíte zcela nové národní prostředí ve svém obchodě, má smysl duplikovat všechny položky obsahu v existujícím národním prostředí do nového národního prostředí. Pokud má nové národní prostředí stejný základní jazyk jako jedno ze stávajících národních prostředí, můžete existující národní prostředí použít jako zdrojové národní prostředí pro operaci kopírování národního prostředí. (Například národní prostředí „en-us“ a „en-au“ používají anglický jazyk.) Tímto způsobem pomůžete snížit množství práce potřebné k lokalizaci obsahu v novém národním prostředí.

Následující postupy vysvětlují, jak přidat nové národní prostředí do existujícího kanálu, zkopírovat všechny položky obsahu z existujícího národního prostředí do nového národního prostředí a jak monitorovat stav operace kopírování národního prostředí.

## <a name="add-a-new-locale"></a>Přidání nového národního prostředí

Nové národní prostředí přidáte v konfigurátoru webů Commerce tímto postupem.

1. V tvůrci webů přejděte na svůj web.
1. V levém navigačním podokně vyberte **Nastavení webu** a pak vyberte **Kanály**.
1. V části **Kanál** vyberte kanál, do kterého chcete přidat nové národní prostředí.
1. V dialogovém okně kanálu, které se zobrazí vpravo, vyberte **Přidat národní prostředí**.
1. V dialogovém okně **Přidat národní prostředí** v poli **Národní prostředí k podpoře** vyberte národní prostředí.
1. Potvrďte, že hodnota **Doména** je správná.
1. V části **Cesta** zadejte jedinečnou cestu adresy URL (např. **en-us** nebo **english-us**).
1. Vyberte **OK**.
1. Zavřete dialogové okno kanálu.
1. V části **Kanál** potvrďte, že je nové národní prostředí uvedeno vedle správného kanálu.
1. Vyberte možnost **Uložit a publikovat**.

> [!NOTE]
> Než bude možné nové národní prostředí nakonfigurovat v konfigurátoru webů, musí být přidáno do přidruženého kanálu online obchodu v Commerce headquarters.

## <a name="copy-all-content-items-to-a-new-locale"></a>Zkopírujte všechny položky obsahu do nového národního prostředí

Všechny položky obsahu zkopírujete do nového národního prostředí v konfigurátoru webů Commerce tímto postupem.

1. V tvůrci webů přejděte na svůj web.
1. V levém navigačním podokně vyberte **Nastavení webu** a pak vyberte **Kanály**.
1. Na panelu příkazů vyberte **Vytvořit kopii národního prostředí z**.
1. V dialogovém okně **Vytvořit kopii národního prostředí**, které se zobrazí vpravo pod **Zdrojový web**, potvrďte, že je vybrán správný web.
1. V poli **Zdrojový kanál** vyberte zdrojový kanál.
1. V poli **Cílový kanál** vyberte stejný zdrojový kanál.
1. V poli **Zdrojové národní prostředí** vyberte zdrojové národní prostředí.
1. V poli **Cílové národní prostředí** vyberte nové národní prostředí.
1. Vyberte **Kopírovat národní prostředí**. Oznámení potvrdí, že byla zahájena operace kopírování národního prostředí.

> [!NOTE]
> Můžete také kopírovat obsah mezi různými kanály.

## <a name="monitor-the-status-of-the-locale-copy"></a>Sledujte stav kopie národního prostředí

Chcete-li sledovat stav operace kopírování národního prostředí, postupujte takto.

1. V tvůrci webů přejděte na svůj web.
1. V levém navigačním podokně vyberte **Nastavení webu** a pak vyberte **Úlohy**.
1. Pod **Aktuální úlohy** vyberte úlohu, kterou chcete sledovat. Informace o úloze se zobrazí v dialogovém okně, které zobrazí vpravo.
