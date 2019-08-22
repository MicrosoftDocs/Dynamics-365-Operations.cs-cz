---
title: Průvodce řešením potíží s integrací dat
description: Toto téma obsahuje informace o odstraňování potíží s integrací dat mezi Microsoft Dynamics 365 for Finance and Operations a Common Data Service.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797268"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Průvodce řešením potíží s integrací dat

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Povolení sledování modulu plug-in v Common Data Service a kontrola podrobností o chybě modulu plug-in dvojího zápisu

Pokud čelíte problému nebo chybě při synchronizaci s dvojím zápisem, můžete zkontrolovat chyby v protokolu sledování:

1. Před tím, než budete moci zkontrolovat chyby, je nutné povolit sledování modulů plug-in pomocí pokynů v části [Registrace modulu plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) pro povolení sledování modulů plug-in. Nyní můžete zkontrolovat chyby.
2. Přihaste se do Dynamics 365 for Sales.
3. Klikněte na ikonu Nastavení (ozubené kolo) a vyberte možnost **Pokročilá nastavení**.
4. V nabídce **Nastavení** vyberte **Přizpůsobení > Protokol sledování modulu plug-in**.
5. Chcete-li zobrazit podrobnosti o chybě, klikněte na název typu **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Kontrola chyb synchronizace s dvojím zápisem v aplikaci Finance and Operations

Chyby můžete zkontrolovat při testování pomocí následujících kroků:

+ Přihlaste se do LifeCycle Services (LCS).
+ Otevřete projekt LCS, který jste zvolili pro testování dvojího zápisu.
+ Přejděte do prostředí hostovaných na cloudu.
+ Vzdálená plocha pro Finance and Operations VM pomocí místního účtu, který je zobrazen v LCS.
+ Otevřít prohlížeč událostí. 
+ Přejděte na **Protokoly aplikací a služeb > Microsoft > Dynamics > AX-DualWriteSync > Provozní**. Zobrazí se chybové zprávy a podrobnosti.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Jak odpojit a propojit jiné prostředí Common Data Service z Finance and Operations

Propojení můžete aktualizovat pomocí následujících kroků:

+ Přejděte do prostředí Finance and Operations.
+ Otevřete správu dat.
+ Klikněte na **Odkaz na CDS for apps**.
+ Vyberte všechna spuštěná mapování a klikněte na **Zastavit**. 
+ Vyberte všechna mapování a klikněte na **Odstranit**.

    > [!NOTE]
    > Volba **Odstranit** se neobjeví, pokud je vybrána šablona **CustomerV3-Account**. V případě potřeby výběr zrušte. **CustomerV3-Account** je starší zřízená šablona a spolupracuje s řešením Zpeněžení potenciálního zákazníka. Protože je globálně vydaná, zobrazí se pod všemi šablonami.

+ Klikněte na **Odpojit prostředí**.
+ Potvrďte kliknutím na **Ano**.
+ Chcete-li nové prostředí propojit, postupujte podle pokynů v [instalační příručce](https://aka.ms/dualwrite-docs).

