---
title: Začínáme s modulem Globální účetnictví zásob
description: Tento článek popisuje, jak začít s globálním účetnictvím zásob.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cbe6bff6fab96900b8bd4e112a8858363fff86d1
ms.sourcegitcommit: 9870b773a2ea8f5675651199fdbc63ca7a1b4453
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013548"
---
# <a name="get-started-with-global-inventory-accounting"></a>Začínáme s modulem Globální účetnictví zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Globální účetnictví zásob umožňuje provádět účetnictví pro více skladů ve vámi vytvořených hlavních knihách globálního účetnictví zásob. Jednotlivé hlavní knihy globálního účetnictví zásob je nutné přidružit ke *konvencím*. Konvence je kolekce následujících typů zásad účetnictví:

- Objekt nákladů
- Základ pro měření vstupu
- Předpoklad toku nákladů
- Prvek nákladů

> [!NOTE]
> I po zapnutí služby Globálního účetnictví zásob můžete v systému Microsoft Dynamics 365 Supply Chain Management stále provádět skladové účetnictví obvyklým způsobem.

Globální účetnictví zásob je doplněk. Chcete-li zpřístupnit její funkce, musíte ji nainstalovat z Microsoft Dynamics Lifecycle Services (LCS). Můžete ji vyhodnotit v testovacím prostředí před tím, než ji zapnete v provozním prostředí.

Globální účetnictví zásob v současné době nepodporuje všechny funkce správy nákladů, které jsou integrovány do Supply Chain Management. Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici, bude vyhovovat vašim požadavkům.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>Jak získat doplněk globálního účetnictví zásob

> [!IMPORTANT]
> Chcete-li použít globální účetnictví zásob, musíte mít prostředí s vysokou dostupností LCS (nikoli prostředí OneBox). Kromě toho musíte používat Supply Chain Management verze 10.0.19 nebo novější.

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management verze 10.0.19 až 10.0.26

Chcete-li nainstalovat Globální účetnictví zásob pro Supply Chain Management verze 10.0.19 až 10.0.26, začněte [instalací doplňku](#install). Poté zašlete své ID prostředí LCS a název společnosti e-mailem na adresu [týmu Globálního účetnictví zásob](mailto:GlobalInvAccount@microsoft.com). Tým vám pošle následný e-mail, který obsahuje koncové body služby globálního účetnictví zásob.

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Management verze 10.0.27 a novější

Chcete-li nainstalovat Globální účetnictví zásob pro Supply Chain Management verze 10.0.27 a novější, stačí [nainstalovat doplněk](#install). Pro tyto verze Supply Chain Management budou koncové body služby Globální účetnictví zásob nastaveny automaticky, takže je nemusíte hledat ručně. Pokud při nastavování doplňku narazíte na nějaké problémy, kontaktujte [tým globálního účetnictví zásob](mailto:GlobalInvAccount@microsoft.com).

## <a name="licensing"></a>Licence

Globální účetnictví zásob je licencováno společně se standardními funkcemi skladového účetnictví, které jsou k dispozici pro řešení Supply Chain Management. Chcete-li používat Globální účetnictví zásob, nemusíte kupovat další licenci.

## <a name="prerequisites"></a>Předpoklady

### <a name="set-up-microsoft-power-platform-integration"></a>Nastavit integraci aplikace Microsoft Power Platform

Než budete moci povolit funkce doplňku, musíte jej integrovat s Microsoft Power Platform provedením těchto kroků.

1. Otevřete prostředí LCS, do kterého chcete službu přidat.
1. Přejděte na **Úplné podrobnosti**.
1. V části **Integrace Power Platform** vyberte **Nastavení**.
1. V dialogovém okně **Nastavení prostředí Power Platform** zaškrtněte políčko a poté vyberte **Založit**. Nastavení obvykle trvá 60 až 90 minut.
1. Po nastavení prostředí Microsoft Power Platform stránka zobrazí název vašeho prostředí. Navíc je v sekci **Integrace Power Platform** uvedena věta „Nastavení prostředí Power Platform je dokončeno.“ Globální účetnictví zásob nevyžaduje aplikaci pro dvojí zápis.

Další informace naleznete v tématu [Aktivace po nasazení prostředí](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="install-the-add-in"></a><a name="install"></a>Instalace doplňku

Podle těchto pokynů nainstalujte doplněk, abyste mohli používat Globální účetnictví zásob.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index).
1. Otevřete prostředí LCS, do kterého chcete službu přidat.
1. Přejděte na **Úplné podrobnosti**.
1. Přejděte na **Integrace Power Platform** a vyberte **Nastavit**.
1. V dialogovém okně **Nastavení prostředí Power Platform** zaškrtněte políčko a poté vyberte **Založit**. Nastavení obvykle trvá 60 až 90 minut.
1. Po nastavení prostředí Microsoft Power Platform se přihlaste do [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com) a poté nainstalujte doplněk Global Inventory Accounting provedením následujících kroků:
   1. Vyberte prostředí, do kterého chcete doplněk nainstalovat.
   1. Vyberte **Aplikace Dynamics 365**.
   1. Vyberte **Nainstalovat aplikaci**.
   1. Vyberte **Globální účetnictví zásob Dynamics 365**.
   1. Instalujte výběrem tlačítka **Další**.
1. Přejděte zpět do prostředí LCS. Na pevné záložce **Doplňky prostředí** vyberte **Nainstalujte nový doplněk**.
1. Vyberte **Globální účetnictví zásob**.
1. Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.
1. Vyberte **Instalovat**.
1. Na záložce s náhledem **Doplňky prostředí** byste měli vidět, že je instalována služba Globální účetnictví zásob. Po několika minutách by se stav měl změnit z *Probíhá instalace* na *Nainstalováno*. (Tato změna se může projevit až po aktualizaci stránky.) V tomto okamžiku je Globální účetnictví zásob připraveno k použití.

Pokud výchozí jazyk vaší instalace Dataverse není angličtina, postupujte podle těchto kroků:
1. Přejděte do **Pokročilé nastavení \> Správa \> Jazyky**.
1. Vyberte *Angličtina* (*LanguageCode = 1033*) a vyberte **Použít**.

## <a name="set-up-the-integration"></a>Nastavení integrace

Pomocí těchto kroků nastavíte integraci mezi Globálním účetnictvím zásob a Supply Chain Management.

1. Přihlaste se k aplikaci Supply Chain Management.
1. Přejděte do nabídky **Správa systému \> Správa funkcí**.
1. Vyberte možnost **Zkontrolovat aktualizace**.
1. Na kartě **Všechny** vyhledejte pojmenovanou funkci *(Preview) Globální účetnictví zásob*.
1. Vyberte **Povolit**.
1. Přejděte na **Globální účetnictví zásob \> Nastavit \> Parametry Globálního účetnictví zásob \> Parametry integrace**.
1. Proveďte jeden z následujících kroků v závislosti na verzi Supply Chain Management, kterou používáte:
    - **Supply Chain Management verze 10.0.19 až 10.0.26** : Do polí **Koncový bod datové služby** a **Koncový bod Globálního účetnictví zásob** zadejte adresy URL, které vám byly zaslány e-mailem od týmu globálního účetnictví zásob (viz také [Jak získat doplněk Globální účetnictví zásob](#sign-up)).
    - **Supply Chain Management verze 10.0.27 a novější**: Nemusíte zadávat koncové body, takže tento krok můžete přeskočit.

Globální účetnictví zásob je nyní připraveno k použití.
