---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Talent (23. července 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 360574d3c8e0b349119e0987f2453a5d5be21e90
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528140"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-23-2019"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Talent (23. července 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="pdf-renderer-for-candidate-documents"></a>Prohlížeč PDF pro dokumenty uchazeče

Uživatelé aplikace Attract nyní mohou prohlížet přílohy PDF pro uchazeče v prohlížeči dokumentů namísto stahování příloh.

### <a name="signing-up-for-attract-user-research-group"></a>Přihlášení ke skupině průzkumu uživatelů Attract 

Jak plánujeme nové možnosti produktu nebo vydáváme funkce náhledu, chceme, aby nám naši uživatelé pomáhali s informacemi o našem směrování. Zúčastnění uživatelé se nyní mohou stát součástí naší výzkumné skupiny uživatelů pomocí odkazu na přihlášení v naší aplikaci.

### <a name="job-approvals-appear-on-the-home-page"></a>Schválení práce se zobrazí na domovské stránce

Schválení se zobrazují v části **Schválení** na řídicím panelu. Schvalovatelé mohou zkontrolovat svá schválení v části **Přiřazeno vám**, která zobrazuje ID práce, pracovní pozici, ostatní schvalovatele a datum přiřazení práce. Uživatelé, kteří odesílají práci ke schválení, mohou revidovat své práce v části **Vyžádáno vámi**, která zobrazuje schvalovatele, kteří musí schválit odeslanou práci.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR
Změny popsané v této části se vztahují na číslo sestavení 8.1.2394.

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Podpora vlastních polí entity v Common Data Service 

V této verzi **pracovní kalendář** a den v **pracovním kalendáři** nyní podporují vlastní pole v Common Data Service.

### <a name="restrict-leave-types-in-time-off-requests"></a>Omezení typů pracovního volna v žádostech o volno

Organizace mohou nabízet mnoho různých typů volna svým zaměstnancům. Pro zaměstnance však nemusí být vhodné odesílat požadavky na volno u některých typů pracovního volna. Tyto typy pracovního volna mohou být namísto toho spravovány oddělením HR. V této verzi můžete konfigurovat, pro které typy pracovního volna mohou zaměstnanci odesílat žádosti o volno. 

## <a name="in-preview"></a>Náhled

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Funkce Preview jsou povoleny pouze v instancích sandbox.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance **Produkce** nebo **Sandbox**. Instance typu **Sandbox** umožňují dřívější testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance **Produkční**. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance **Sandbox**, obraťte se na [podporu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Zobrazení rozšířených informací o výkonu v samoobsluze pro manažery

Nová možnost umožní, aby manažeři zobrazili výkon svých přímých podřízených i jejich rozšířených podřízených. V současné době mohou linioví manažeři přiřazovat a aktualizovat cíle výkonnosti a vydávat nové revize, na kterých jejich zaměstnanci spolupracují. Kromě toho mohou přímí manažeři a jejich zaměstnanci udržovat a aktualizovat deníky výkonnosti, aby byl zajištěn plynulý proces kontroly výkonu. Při implementaci této změny budou mít manažeři možnost zobrazit a udržovat informace související s výkonem pro své rozšířené podřízené spolu se svými přímými podřízenými. 

## <a name="coming-soon"></a>Již brzy

### <a name="region-support-for-canada-and-southeast-asia"></a>Regionální podpora pro Kanadu a jihovýchodní Asii

S radostí oznamujeme, že od 1. srpna 2019 bude Talent k dispozici pro Kanadu a jihovýchodní Asii. Tato změna umožňuje vytvářet prostředí v kanadských a asijských oblastech a všechna data aplikace Talent budou zachována pouze v těchto umístěních. Prostředí v těchto nových oblastech můžete vytvořit výběrem umístění v dialogovém okně Nové prostředí a použitím tohoto prostředí ke zřizování aplikace v rámci LCS, jak je popsáno zde: [Zřizování aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Migrace dat existujících projektů z jiných oblastí do kanadských a asijských oblastí není podporována. Pro tyto nové podporované oblasti lze zřizovat pouze nové projekty.
