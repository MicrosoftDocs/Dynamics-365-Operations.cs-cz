---
title: Odstraňování problémů s upgradem a migrací na pokročilou správu skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s upgradem a migrací na pokročilou správu skladu.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993859"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Odstraňování problémů s upgradem a migrací na pokročilou správu skladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s upgradem a migrací na pokročilou správu skladu.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Zobrazuje se následující chybová zpráva: „java.security.cert.certPathValidatorException: Nebyla nalezena důvěryhodná kotva pro certifikační cestu.“

### <a name="issue-description"></a>Popis problému

Tato chybová zpráva se zobrazí v aplikaci skladu, protože certifikáty podepsané svým držitelem nejsou důvěryhodné v Android 8+ v místních prostředích.

### <a name="issue-resolution"></a>Řešení problému

Použijte externí (veřejný) certifikační autoritu (CA). Oprava tohoto problému je k dispozici ve verzi 1.9.0.0 aplikace skladu. Další informace o tomto problému a jeho řešení najdete v tématu [Odstraňování problémů s připojením aplikace skladu](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Jaký je schválený proces přechodu od základního skladování k pokročilému skladování?

### <a name="issue-description"></a>Popis problému

Momentálně běžíte pod správou skladu/zásob a používáte základní funkce skladu a chcete přejít na pokročilé skladování, abyste mohli využívat výhod mobilních zařízení, vln a práce. Při pokusu o tento krok však dochází k problémům. Například nemůžete změnit své produkty tak, aby používaly dimenze úložiště (web, sklad a umístění), protože produkty mají proti nim transakce. Musíte se tedy naučit schválený proces přechodu od základního skladování k pokročilému skladování.

### <a name="issue-resolution"></a>Řešení problému

Další informace o procesu přechodu ze základního skladování na pokročilé skladování najdete v následujících příspěvcích na blogu a v dokumentaci:

- [Povolit procesy správy skladu pro existující položky a sklady](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Migrace Microsoft Dynamics AX WMS do nové skladové a přepravní funkce R3](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [Migrace položek WMSI/WMS2](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Upgrade správy skladu z Microsoft Dynamics AX 2012 do Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]