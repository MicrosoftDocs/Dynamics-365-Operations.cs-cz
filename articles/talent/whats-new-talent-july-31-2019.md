---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Talent (30. července 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 311042caf6a391a06c7e2d8c4c2c2f6e1f855437
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460601"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-30-2019"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Talent (30. července 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR
Změny popsané v této části se vztahují na číslo sestavení 8.1.2409.


### <a name="region-support-for-canada-and-southeast-asia"></a>Regionální podpora pro Kanadu a jihovýchodní Asii

S radostí oznamujeme, že od 1. srpna 2019 bude Talent k dispozici pro Kanadu a jihovýchodní Asii. Tato změna umožňuje vytvářet prostředí v kanadských a asijských oblastech a všechna data aplikace Talent budou zachována pouze v těchto umístěních. Prostředí v těchto nových oblastech můžete vytvořit výběrem umístění v dialogovém okně Nové prostředí a použitím tohoto prostředí ke zřizování aplikace v rámci LCS, jak je popsáno v tématu [Zřizování aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Migrace dat existujících projektů z jiných oblastí do kanadských a asijských oblastí není podporována. Pro tyto nové podporované oblasti lze zřizovat pouze nové projekty.

### <a name="new-active-positions-list-page"></a>Stránka se seznamem Nové aktivní pozice

Možnosti pro seznamy založené na pozicích nyní zahrnují: **všechny pozice**, **aktivní pozice**, **otevřené pozice** a **neaktivní pozice**. Nová stránka se seznamem **Aktivní pozice** zobrazuje pouze pozice, otevřené nebo vyplněné, které jsou aktivní k aktuálnímu datu. 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a>Povolení přidávání účastníků kurzu do otevřených kurzů

Tato změn týdne opravuje problém, kdy lze na otevřené kurzy registrovat pouze přímé podřízené.

### <a name="fte-analysis-displaying-incorrect-fte-number"></a>Analýza FTE zobrazující nesprávné číslo FTE

**Analýza FTE** byla opravena na kartě **Analýzy** v okně **Správa zaměstnanců**.

### <a name="final-comments-label-translation"></a>Překlad popisku závěrečných komentářů

Popisek **Závěrečné komentáře** je nyní přeložen ve formuláři Revize.

## <a name="in-preview"></a>Náhled

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Funkce Preview jsou povoleny pouze v instancích sandbox.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance **Produkce** nebo **Sandbox**. Instance typu **Sandbox** umožňují dřívější testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance **Produkční**. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance **Sandbox**, obraťte se na [podporu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Zobrazení rozšířených informací o výkonu v samoobsluze pro manažery

Nová možnost umožní, aby manažeři zobrazili výkon svých přímých podřízených i jejich rozšířených podřízených. V současné době mohou linioví manažeři přiřazovat a aktualizovat cíle výkonnosti a vydávat nové revize. Kromě toho mohou přímí manažeři a jejich zaměstnanci udržovat a aktualizovat deníky výkonnosti, aby byl zajištěn plynulý proces kontroly výkonu. Při implementaci této změny budou mít manažeři možnost zobrazit a udržovat informace související s výkonem pro své rozšířené podřízené spolu se svými přímými podřízenými.
