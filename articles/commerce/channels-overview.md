---
title: Přehled kanálů
description: Toto téma poskytuje přehled kanálů v Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 64dcb02e9d35f530ea498c65473a98de3d18912e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335707"
---
# <a name="channels-overview"></a>Přehled kanálů


[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled kanálů v Microsoft Dynamics 365 Commerce. Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení každého kanálu.

## <a name="types-of-channels"></a>Typy kanálů

Dynamics 365 Commerce podporuje tři různé typy kanálů: maloobchodní, kontaktní a online kanály.

### <a name="retail-channels"></a>Maloobchodní sítě

Maloobchodní kanály představují standardní kamenné obchody. Každý obchod může mít vlastní pokladní místo (POS), účty příjmů a výdajů a zaměstnance. 

### <a name="call-center-channels"></a>Kanály kontaktního střediska

Kanály kontaktního střediska reprezentují objednávku střediska volání a řízení zákazníků.

### <a name="online-channels"></a>Online kanály

Online kanály představují online poutače e-Commerce. Po vytvoření online kanálu je nutné vytvořit web pomocí nástroje Microsoft Dynamics 365 Commerce Site Builder nebo jiného řešení e-Commerce třetí strany.

## <a name="channel-setup-basics"></a>Základy nastavení kanálu

Nastavení kanálu se provádí v nástroji Commerce. Každý kanál může mít vlastní metody platby, cenové skupiny, hierarchie produktů, sortimenty a sadu produktů. Po vytvoření kanálu přiřadíte produkty, které má obsahovat a prodávat. Každý typ kanálu má jedinečnou sadu funkcí, které je nutné nakonfigurovat. Maloobchodní kanál například vyžaduje přiřazení zaměstnanců, registrů a odběratelů. Jakmile je vytvořen nový kanál, musí být přiřazen k organizační hierarchii.

## <a name="channel-setup-prerequisites"></a>Předpoklady nastavení kanálu

Před nastavením kanálu je nutné dokončit některé požadované úkoly na základě typu kanálu. Další informace naleznete v tématu [Předpoklady pro nastavení kanálů](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Nastavení kanálu

Po dokončení požadovaných úloh proveďte další pokyny k instalaci aplikace pomocí následujících odkazů.

- [Nastavení maloobchodního kanálu](channel-setup-retail.md)
- [Nastavení kanálu kontaktního střediska](channel-setup-callcenter.md)
- [Nastavení online kanálu](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Další zdroje

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Nastavení maloobchodního kanálu](channel-setup-retail.md)
    
[Nastavení online kanálu](channel-setup-online.md)

[Nastavení kanálu kontaktního střediska](channel-setup-callcenter.md)

[Nastavení organizačních hierarchií](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]