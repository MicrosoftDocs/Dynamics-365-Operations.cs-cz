---
title: Možnosti implementace sítě pro doručování obsahu
description: V tomto tématu jsou uvedeny různé možnosti implementace sítě pro doručování obsahu (CDN), které lze použít s prostředím Microsoft Dynamics 365 Commerce. Mezi tyto možnosti patří nativní instance služby Azure Front Door poskytované Commerce a instance Azure Front Door vlastněné zákazníky.
author: BrianShook
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f6e8fb2baf85be0eaecfffcc7ec6cbb457c3bb04
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021883"
---
# <a name="content-delivery-network-implementation-options"></a>Možnosti implementace sítě pro doručování obsahu

[!include [banner](includes/banner.md)]

V tomto tématu jsou uvedeny různé možnosti implementace sítě pro doručování obsahu (CDN), které lze použít s prostředím Microsoft Dynamics 365 Commerce. Mezi tyto možnosti patří nativní instance služby Azure Front Door poskytované Commerce a instance Azure Front Door vlastněné zákazníky.

Zákazníci Commerce mají několik možností, když uvažují, kterou službu CDN použít ve svém Commerce prostředí. Commerce je vydáván se základní podporou Azure Front Door, která pokrývá základní požadavky na hostování a vlastní doménu. Pro společnosti, které chtějí větší kontrolu a konkrétnější možnosti zabezpečení, jako je brána firewall webových aplikací (WAF), může být nejlepší volbou použít buď instanci Azure Front Door, kterou vlastní zákazník, nebo externí službu CDN.

V prostředích Commerce lze použít následující tři možnosti implementace CDN:

- Instance Azure Front Door poskytnutá Commerce
- Instance Azure Front Door vlastněná zákazníkem (pro lepší kontrolu a další funkce zabezpečení)
- Externí služba CDN

Všechny tři možnosti implementace CDN dodávají pouze dynamický obsah HTML z vlastních domén. Commerce automaticky zpracovává všechny JavaScript, kaskádové styly (CSS), obrázky, videa a další statický obsah prostřednictvím sítí CDN spravovaných společností Microsoft. Možnost, kterou vyberete, určuje operační schopnosti, možnosti ovládání a další možnosti zabezpečení, které jsou k dispozici.

Následující obrázek přehledně znázorňuje přehled architektury Commerce.

![Přehled architektury Commerce](media/Commerce_CDN-Option_ComparisonModels.png)

Další informace o tom, jak nastavit instanci Azure Front Door pro váš web Commerce, viz [Přidání podpory CDN](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Použití instance Azure Front Door poskytnuté Commerce

V následující tabulce jsou uvedeny výhody a nevýhody používání instance Azure Front Door poskytované Commerce ke správě koncových bodů obsahu.

| Výhody | Nevýhody |
|------|------|
| <ul><li>Instance je zahrnuta v ceně Commerce.</li><li>Protože instance je spravována týmem Commerce, je vyžadována menší údržba a existují sdílené kroky instalace.</li><li>Infrastruktura hostovaná v Azure je škálovatelná, bezpečná a spolehlivá.</li><li>Certifikát SSL (Secure Sockets Layer) vyžaduje jednorázové nastavení a je automaticky obnovován.</li><li>Instance je monitorována z hlediska chyb a anomálií týmem Commerce.</li></ul> | <ul><li>WAF není podporována.</li><li>Neexistují žádná konkrétní přizpůsobení nebo úpravy nastavení.</li><li>Instance závisí na aktualizaci nebo změnách týmu Commerce.</li><li>Pro vrcholové domény je vyžadována samostatná instance Azure Front Door a pro integraci vrcholových domén s Azure DNS je zapotřebí další práce.</li><li>Zákazníkovi není poskytována žádná telemetrie o odpovědích za sekundu (RPS) ani chybovost.</li></ul> |

Následující obrázek ukazuje architekturu instance Azure Front Door poskytované Commerce.

![Instance Azure Front Door poskytnuté Commerce](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Použití instance Azure Front Door, kterou vlastní zákazník

V následující tabulce jsou uvedeny výhody a nevýhody používání instance Azure Front Door vlastněné zákazníkem ke správě koncových bodů obsahu.

| Výhody | Nevýhody |
|------|------|
| <ul><li>Nastavení je bezpečné a snadno se spravuje.</li><li>Infrastruktura hostovaná v Azure je škálovatelná, bezpečná a spolehlivá.</li><li>Instance umožňuje integraci WAF a ovládací prvky granulárních pravidel pro jemnější zabezpečení, které je vyladěno speciálně pro váš web.</li><li>Instance umožňuje jemnější kontrolu nad certifikáty SSL (vlastními i spravovanými Azure Front Door) a propojováním domén.</li><li>Instance nabízí řešení vrcholové domény, pokud je spárováno přímo s Azure DNS.</li><li>K dispozici je telemetrie a výstrahy.</li><li>Certifikát SSL vyžaduje jednorázové nastavení a je automaticky obnovován.</li></ul> | <ul><li>Instance je spravována samostatně.</li><li>Je vyžadováno počáteční získávání znalostí.</li></ul> |

Následující obrázek ukazuje infrastrukturu Commerce, která zahrnuje instanci Azure Front Door, kterou vlastní zákazník.

![Infrastruktura Commerce, která zahrnuje instanci Azure Front Door, kterou vlastní zákazník](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Použití externí služby CDN

V následující tabulce jsou uvedeny výhody a nevýhody používání externí služby CDN ke správě koncových bodů obsahu.

| Výhody | Nevýhody |
|------|------|
| <ul><li>Tato možnost je užitečná, když je stávající doména již hostována na externím CDN.</li><li>Konkurenční CDN (například Akamai) mohou mít více funkcí WAF.</li></ul> | <ul><li>Je vyžadována samostatná smlouva a další náklady.</li><li>SSL může způsobit další náklady.</li><li>Protože je služba oddělená od cloudové struktury Azure, je nutné spravovat další infrastrukturu.</li><li>Služba může vyžadovat delší časové investice do nastavení koncového bodu a zabezpečení.</li><li>Služba je spravována samostatně.</li><li>Služba je automaticky monitorována.</li></ul> |

Následující obrázek ukazuje infrastrukturu Commerce, která zahrnuje externí službu CDN.

![Infrastruktura Commerce, která zahrnuje externí službu CDN](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Další prostředky

[Přidání podpory sítě pro doručování obsahu (CDN)](add-cdn-support.md)
