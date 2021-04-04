---
title: Přehled tisku dokumentu
description: Dokumenty můžete tisknout buď pomocí lokální tiskárny nebo zařízení připojeného k síti. Tento článek poskytuje přehled způsobu tisku dokumentů.
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c349e50826aa577ce6a3b8a68676d549f7fed1b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564398"
---
# <a name="document-printing-overview"></a>Přehled tisku dokumentu

[!include [banner](../includes/banner.md)]

Dokumenty můžete tisknout buď pomocí lokální tiskárny nebo zařízení připojeného k síti. Tento článek poskytuje přehled způsobu tisku dokumentů.

## <a name="printing-overview"></a>Přehled tisku

Aplikace poskytuje integrované služby a klientské aplikace, které usnadňují generování, ukládání a distribuci dokumentů, které podporují podnikatelské aktivity. Dokumenty můžete tisknout buď pomocí lokální tiskárny nebo zařízení připojeného k síti. Kromě toho můžete exportovat stránky a sestavy aplikace přímo z klienta jako soubory PDF nebo dokumenty Microsoft Office. V neposlední řadě vám distribuované pracovní vytížení umožňuje tisknout obchodní dokumenty přímo z mobilní zařízení pomocí síťových prostředků. Přestože se požadavky na tisk mohou lišit, všechna odvětví obvykle musí vytvářet tištěné kopie obchodních dokumentů pomocí aplikace. Tisk dokumentů na síťových zařízeních z hostovaných aplikací představuje ojedinělou řadu výzev. Několik příkladů:

- Tiskové ovladače nemusí být k dispozici na zařízeních uživatele.
- Zařízení uživatele nemusí být připojeno k firemní síti.

Pomocí vyhrazeného hostitele a několika jednoduchých kroků mohou správci systému nakonfigurovat nasazení tak, aby uživatelé mohli tisknout přímo z podnikových aplikací na síťových zařízeních.

### <a name="application-printing-scenarios"></a>Scénáře tisku aplikací 

V následující tabulce jsou popsány tři hlavní scénáře tisku.

| Scénář                        | Cíl                                                      | Řešení |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Tisk toho, co vidíte        | Tiskněte to, co je momentálně zobrazeno v prohlížeči.             | Pro prohlížeč se vygeneruje pro tisk vhodná verze webové stránky. |
| 2. Interaktivní tisk         | Tiskněte přesný dokument na místně připojeném zařízení. | Můžete exportovat PDF verzi sestavy a stáhnout ji do prohlížeče. |
| 3. Tisk na síťovém zařízení | Odešlete přesný dokument do domény tiskárny.     | Přesný dokument je odeslán do klientské aplikace spuštěné na serveru, který je hostován v doméně zákazníka. |

Protože se řešení liší, v závislosti na scénáři poskytují aplikace vestavěné služby a nástroje, které uživatelům pomáhají dosáhnout svých cílů:

- **Scénář 1** je podporován vykreslováním prohlížeče HTML5 klienta.
- **Scénář 2** používá aplikace klienta a služeb Microsoft 365.
- **Scénář 3** vyžaduje podporu od aplikací klienta a služeb, které jsou hostovány v Microsoft Azure.

Kromě platformy, která je nasazena do předplatného Azure, aplikace Finance and Operations poskytuje zákazníkům integrovanou aplikaci Azure první strany, která jim pomáhá snadněji využívat zařízení hostovaná na doméně pro tisk dokumentů.

## <a name="service-overview"></a>Přehled služby
Zatímco dokumenty vytvořené hostovanými aplikacemi čekají na tisk na zařízení připojeném k síti, jsou uloženy v úložišti objektu blob Azure. [Instalace agenta směrování dokumentu pro aktivaci síťového tisku](install-document-routing-agent.md) používá ověřování Azure k vytvoření zabezpečeného kanálu do služeb Azure.

**Pořadí spouštění**

1. Sestava je generovaná pomocí aplikace Microsoft SQL Server Reporting Services (SSRS) a uložena do úložiště objektů blob Azure. Nastavení připojené tiskárny jsou uložena spolu s dokumenty.
2. Agent pro směrování dokumentů se dotáže fronty sběrnice služby Azure na aktivní úlohy.
3. Dokument je stažen agentem pro směrování dokumentů a zařazen na síťovou tiskárnu.

Řešení založené na klientovi umožňuje zákazníkům spravovat rozsah jejich tiskových potřeb. Zákazníci, kteří pracují s velkým objemem tisku, mohou nainstalovat mnoho agentů pro směrování dokumentů, aby se zvýšil počet souběžných tiskových operací. Někteří zákazníci oproti tomu vyžadují velmi málo instalací agentů pro směrování dokumentů, aby zvládli své očekávané potřeby tisku.

### <a name="service-components-for-network-printing"></a>Servisní komponenty pro síťový tisk

Následující diagram znázorňuje základní komponenty, které pomáhají s podporou operací síťového tisku.

[![servisní-komponenty-pro-síťový-tisk\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Všimněte si, že jednu tiskárnu lze registrovat s více agenty pro směrování dokumentů. Chcete-li vyřešit předvolby tiskárny, hostovaná služba používá síťovou cestu, která jednoznačně identifikuje každou síťovou tiskárnu. Výsledkem je, že i když je tiskárna registrována více klienty, zobrazí se jako jedna volba v seznamu tiskáren dostupných v aplikacích.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]