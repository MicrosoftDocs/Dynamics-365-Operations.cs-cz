---
title: Podporované scénáře pro nastavení dvojího zápisu
description: Toto téma popisuje scénáře, které jsou podporovány pro nastavení dvojího zápisu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818589"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Podporované scénáře pro nastavení dvojího zápisu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Můžete nastavit připojení dvojího zápisu mezi prostředím Finance and Operations a Common Data Service.

+ **Prostředí Finance and Operations** poskytuje základní platformu pro **aplikace Finance and Operations** (například Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management a Dynamics 365 Retail).
+ **Prostředí Common Data Service** poskytuje základní platformu pro **aplikace řízené modelem Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing a Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Modul personalistiky v aplikaci Finance and Operations podporuje připojení pro duální zápis, ale aplikace Dynamics 365 Human Resources ne.

Nastavení mechanismu se liší v závislosti na vašem předplatném a prostředí.

+ U nových instancí aplikací Finance and Operations začíná nastavení připojení dvojího zapisování v Lifecycle Services (LCS) Microsoft Dynamics. Máte-li licenci pro Power Platform, obdržíte nové prostředí Common Data Service, pokud je váš klient neobsahuje.
+ Pro existující instance aplikací Finance and Operations začíná nastavení připojení dvojího zapisování do prostředí Finance and Operations.

Podporovány jsou následující scénáře registrace:

+ [Nová instance aplikace Finance and Operations a nová instance aplikace řízené modelem](#new-new)
+ [Nová instance aplikace Finance and Operations a existující instance aplikace řízené modelem](#new-existing)
+ [Nová instance aplikace Finance and Operations, která má ukázková data, a nová instance aplikace řízené modelem](#new-demo-new)
+ [Nová instance aplikace Finance and Operations, která má ukázková data, a existující instance aplikace řízené modelem](#new-demo-existing)
+ [Existující instance aplikace Finance and Operations a nová nebo existující instance aplikace řízené modelem](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Nová instance aplikace Finance and Operations a nová instance aplikace řízené modelem

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a novou instanci aplikace řízené modelem v aplikaci Dynamics 365, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md). Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:

- Je zajištěno nové prázdné prostředí Finance and Operations.
- Je zřízena nová prázdná instance aplikace řízené modelem, kde je nainstalováno základní řešení CRM.
- Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.
- Mapování entit je povoleno pro živou synchronizaci.

Obě prostředí jsou připravena k synchronizaci dat živého vysílání.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Nová instance aplikace Finance and Operations a existující instance aplikace řízené modelem

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která neobsahuje žádná data a existující instanci aplikace řízené modelem v aplikaci Dynamics 365, postupujte podle kroků v [nastavení dvojího zápisu z Lifecycle Services](lcs-setup.md). Po dokončení nastavení připojení dojde k automatickému provedení následujících akcí:

- Je zajištěno nové prázdné prostředí Finance and Operations.
- Pro data společnosti DAT je vytvořeno připojení s dvojím zapisováním.
- Mapování entit je povoleno pro živou synchronizaci.

Obě prostředí jsou připravena k synchronizaci dat živého vysílání.

Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, postupujte podle následujících kroků.

1. Vytvořte v aplikaci Finance and Operations novou společnost.
2. Přidejte společnost do nastavení připojení s duálním zapisováním.
3. [Zavedení](bootstrap-company-data.md) dat Common Data Service pomocí třímístného kódu společnosti pro Mezinárodní organizaci pro normalizaci (ISO).

Vzhledem k tomu, že dvojí zapisování je v režimu synchronizace živého vysílání, data aplikace Common Data Service automaticky začnou proudit do aplikace Finance and Operations.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Nová instance aplikace Finance and Operations, která má ukázková data, a nová instance aplikace řízené modelem

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má ukázková data, a novou instanci aplikace řízené modelem v aplikaci Dynamics 365, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v oddílu nové instance aplikace řízené podle modelu](#new-new) dříve v tomto tématu. Chcete-li v aplikaci synchronizovat ukázková data s aplikací řízenou modelem, postupujte po dokončení nastavení připojení následujícím způsobem.

1. Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.
2. Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Nová instance aplikace Finance and Operations, která má ukázková data, a existující instance aplikace řízené modelem

Chcete-li nastavit připojení dvojího zapisování mezi novou instancí aplikace Finance and Operations, která má ukázková data, a existující instanci aplikace řízené modelem v aplikaci Dynamics 365, postupujte podle kroků v [nové instanci aplikace Finance and Operations a v existující instanci aplikace řízené podle modelu](#new-existing) dříve v tomto tématu. Chcete-li v aplikaci synchronizovat ukázková data s aplikací řízenou modelem, postupujte po dokončení nastavení připojení následujícím způsobem.

1. Otevřete aplikaci Finance and Operations ze stránky LCS, přihlaste se a pak přejděte ke **Správě dat \> Dvojí zápis**.
2. Spusťte funkci **Počáteční synchronizace** pro entity, pro které chcete synchronizovat data.

Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, postupujte podle následujících kroků.

1. Vytvořte v aplikaci Finance and Operations novou společnost.
2. Přidejte společnost do nastavení připojení s duálním zapisováním.
3. [Zavedení](bootstrap-company-data.md) dat Common Data Service pomocí třímístného kódu společnosti ISO.

Vzhledem k tomu, že dvojí zapisování je v režimu synchronizace živého vysílání, data aplikace Common Data Service automaticky začnou proudit do aplikace Finance and Operations.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Existující instance aplikace Finance and Operations a nová nebo existující instance aplikace řízené modelem

Nastavení připojení s dvojím zapisováním mezi existující instancí aplikace Finance and Operations a novou nebo existující instancí aplikace řízené modelem v aplikaci Dynamics 365 probíhá v prostředí Finance and Operation.

1. Nastavit připojení z aplikace Finance and Operations
2. Chcete-li synchronizovat existující data Common Data Service s aplikací Finance and Operations, [zaveďte](bootstrap-company-data.md) data Common Data Service pomocí třímístného kódu ISO společnosti.

Vzhledem k tomu, že dvojí zapisování je v režimu synchronizace živého vysílání, data aplikace Common Data Service automaticky začnou proudit do aplikace Finance and Operations.
