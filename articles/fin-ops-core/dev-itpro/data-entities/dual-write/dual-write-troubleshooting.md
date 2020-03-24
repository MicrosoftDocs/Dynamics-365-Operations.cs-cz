---
title: Průvodce řešením potíží s integrací dat
description: Toto téma obsahuje informace o odstraňování potíží pro integrací dat mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 87bdb72024c1c3844ff61e832a92f7edcc77c5d6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019681"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Průvodce řešením potíží s integrací dat

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Povolení protokolů sledování modulu plug-in v Common Data Service a kontrola podrobností o chybě modulu plug-in dvojího zápisu

Pokud při synchronizaci dvojího zápisu dojde k problému nebo chybě, postupujte podle následujících kroků ohledně kontroly chyb v protokolu sledování.

1. Před kontrolou chyb je nutné povolit protokoly sledování modulů plug-in. Pokyny naleznete v části Zobrazení protokolů sledování [Kurzu: Zápis a registrace modulu plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Nyní můžete zkontrolovat chyby.

2. Přihlaste se do aplikace Microsoft Dynamics 365 Sales.
3. Vyberte tlačítko **Nastavení** (symbol ozubeného kola) a poté vyberte položku **Pokročilá nastavení**.
4. V nabídce **Nastavení** vyberte **Přizpůsobení \> Protokol sledování modulu plug-in**.
5. Chcete-li zobrazit podrobnosti o chybě, zvolte jako název typu **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.

## <a name="inspect-dual-write-synchronization-errors"></a>Zkontrujte chyby synchronizace dvojího zápisu

Chcete-li kontrolovat chyby během testování, postupujte následujícím způsobem.

1. Přihlaste se do Microsoft Dynamics Lifecycle Services (LCS).
2. Otevřete projekt LCS, pro který chcete provést testování dvojího zápisu.
3. Zvolte **Prostředí hostovaná v cloudu**.
4. Vytvořte připojení ke vzdálené ploše k virtuálnímu počítači aplikace pomocí místního účtu zobrazeného na LCS.
5. Otevřete prohlížeč událostí. 
6. Přejděte na **Protokoly aplikací a služeb \> Microsoft \> Dynamics \> AX -DualWriteSync \> Provozní**. Zobrazí se chybové zprávy a podrobnosti.

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>Odpojte jedno prostředí Common Data Service z aplikace a připojte jiné prostředí

Pro aktualizaci spojení postupujte podle těchto kroků.

1. Přejděte do prostředí aplikace
2. Otevřete správu dat.
3. Zvolte **Odkaz na CDS for Apps**.
4. Vyberte všechna mapování, která jsou spuštěna, a poté vyberte **Zastavit**.
5. Vyberte všechna mapování a poté vyberte možnost **Odstranit**.

    > [!NOTE]
    > Volba **Odstranit** není k dispozici, pokud je vybrána šablona **CustomerV3-Account**. Zrušte výběr této šablony podle potřeby. **CustomerV3-Account** je starší zřízená šablona a spolupracuje s řešením Zpeněžení potenciálního zákazníka. Protože je globálně vydaná, zobrazí se pod všemi šablonami.

6. Zvolte **Odpojit prostředí**.
7. Vyberte **Ano**, chcete-li potvrdit operaci.
8. Chcete-li nové prostředí propojit, postupujte podle pokynů v [instalační příručce](https://aka.ms/dualwrite-docs).