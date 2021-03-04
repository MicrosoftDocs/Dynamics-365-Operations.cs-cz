---
title: Publikování pracovních míst na Broadbean z aplikace Attract
description: Toto téma vysvětluje postup použití aplikace Dynamics 365 Talent - Attract pro publikování pracovních míst ve službě Broadbean
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 41fa057606887069a9ea0f1f2178eeaff59f33ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460611"
---
# <a name="post-jobs-to-broadbean-from-attract"></a>Publikování pracovních míst na Broadbean z aplikace Attract

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract vám pomůže získat talenty, které potřebujete, a to tak, že vám umožní publikovat pracovní místa přímo z Attract na Broadbean. Po [vytvoření pracovního místa](./creating-jobs-attract.md) stačí vybrat tlačítko, které přivede vaši pracovní pozici k očím tisíců možných kandidátů na pracovní pozici ve službě Broadbean.

Zveřejňování pracovních míst ve službě Broadbean vyžaduje příslušnou licenci Broadbean. Broadbean nabízí různé produkty a plány. Další informace o licencování a cenách ve službě Broadbean [vám poskytne společnost Broadbean](https://www.broadbean.com/contact-us/).

Pokud jste správce, který potřebuje více informací o postupu konfigurace integrace Broadbean s Attract, získáte informace v části [Povolení integrace služby Broadbean integration v aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-admin-job-board-settings.md).

## <a name="post-jobs-to-broadbean"></a>Publikování pracovních míst na Broadbean

Po zapnutí Broadbean mohou náboroví pracovníci a správci na tomto webu publikovat pracovní místo. Pro úlohu musíte mít adresu URL žádosti.

1. V aplikaci Attract otevřete práci, kterou chcete publikovat na Broadbean.
2. V části **Publikování** zvolte tlačítko **Publikovat nyní**, které odpovídá Broadbeanu.
3. Postupujte podle pokynů v okně Broadbean.

Attract předává Broadbeanu následující informace:

- ID požadavku
- Pracovní titul
- Popis úlohy
- Místo výkonu práce
- URL adresu žádosti
- Informace náborového pracovníka

Po úspěšném dokončení publikace na Broadbeanu zobrazí část práce **Publikování** v aplikaci Attract stav Broadbean jako **Publikováno**.

> [!NOTE]
> - Broadbean vyžaduje pole **Obor**. Momentálně je toto pole ve výchozím nastavení nastaveno na **IT**. Hodnotu však můžete změnit na správné obor v okně pro publikování práce Broadbean.
> - Trvá nějakou dobu, než Broadbean dokončí publikování vaší práce na všechny vývěsky, které jste vybrali. Proto může dojít k mírnému zpoždění, než Attract poskytne aktualizaci stavu pro práci.

### <a name="view-a-broadbean-job-posting"></a>Zobrazení publikovaného pracovního místa na Broadbeanu

Po publikování pracovního místa ho můžete zobrazit z aplikace Attract.

1. V aplikaci Attract otevřete práci, kterou chcete zobrazit na Broadbeanu.
2. Na kartě **Publikování** vyberte tlačítko s třemi tečkami (**...**), které odpovídá Broadbeanu, a poté vyberte **Zobrazit**.

Publikování pracovního místa na Broadbeanu se zobrazí v novém okně.

### <a name="update-a-broadbean-job-posting"></a>Aktualizace publikovaného pracovního místa na Broadbeanu

Je možné aktualizovat publikované pracovní místo na Broadbeanu dvěma způsoby.

1. V aplikaci Attract otevřete práci, kterou chcete aktualizovat.
2. V části **Publikování** zvolte tlačítko **Aktualizovat publikovanou práci**, které odpovídá Broadbeanu.
3. Upravte publikované pracovní místo v okně Broadbean.

    - nebo -

1. V aplikaci Attract otevřete práci, kterou chcete zobrazit na Broadbeanu.
2. V části **Publikování** zvolte tlačítko s třemi tečkami (**...**), které odpovídá Broadbeanu, a poté vyberte **Zobrazit**.
3. V okně Broadbean upravte podrobnosti práce a pak ji znovu publikujte. Podrobnosti práce v aplikaci Attract se nezmění.

### <a name="remove-a-broadbean-job-posting"></a>Odstranění publikovaného pracovního místa na Broadbeanu

Můžete odstranit publikované pracovní místo z Broadbeanu podle potřeby.

1. V aplikaci Attract otevřete práci, kterou chcete odstranit.
2. V části **Publikování** zvolte tlačítko s třemi tečkami (**...**), které odpovídá Broadbeanu, a poté vyberte **Odstranit publikovanou práci**.

Poté, co Broadbean odebere práci, bude mít položka Broadbean v aplikaci Attract tlačítko **Publikovat nyní**. Přítomnost tohoto tlačítka označuje, že práce byla odstraněna a lze ji znovu publikovat.

### <a name="troubleshoot-job-posting-to-broadbean"></a>Poradce při potížích se zveřejňováním pracovních nabídek ve službě Broadbean

Pokud máte problémy s publikováním pracovního místa na Broadbean, vyzkoušejte následující kroky.

1. Ověřte, zda jsou přihlašovací údaje Broadbean, které jste zadali v aplikaci Attract, platné a správné.
2. Pokud jsou přihlašovací údaje platné a správné, kontaktujte [Broadbean podporu](https://www.broadbean.com/resources/support/).
3. Pokud problém přetrvává, obraťte se na [podporu společnosti Microsoft](./talent-support.md).

## <a name="see-also"></a>Viz také

[Vytvoření, schválení a zveřejnění pracovních míst v aplikaci Attract](./creating-jobs-attract.md)

[Povolení integrace služby Broadbean v aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-admin-job-board-settings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]