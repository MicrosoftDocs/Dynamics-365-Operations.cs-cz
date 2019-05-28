---
title: Publikování pracovních míst z aplikace Attract na externí weby
description: Toto téma vysvětluje postup použití aplikace Dynamics 365 for Talent - Attract pro publikování pracovních míst na externí náborové weby.
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
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
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517529"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Publikování pracovních míst z aplikace Attract na externí weby

[!include [banner](../includes/banner.md)]

Chcete dostat své otevřené pozice před co největší množství kvalifikovaných kandidátů. Náborové weby, například Broadbean, vám pomohou dosáhnout tohoto cíle. Microsoft Dynamics 365 Talent: Attract vám nyní umožní publikovat pracovní místa na Broadbean a Microsoft neustále v této oblasti poskytuje nové nabídky.

## <a name="post-jobs-to-broadbean"></a>Publikování pracovních míst na Broadbean

Před publikováním pracovních míst na Broadbean musíte nakonfigurovat integraci Broadbean.

> [!NOTE]
> - Chcete-li publikovat pracovní místa na externí weby, musíte mít [doplněk komplexního náboru](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Tato funkce je aktuálně v náhledu Pokud chcete provést akci, musíte [ji zapnout v nastavení pro správu Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Konfigurace integrace s Broadbean

1. Přihlaste se do aplikace Attract jako správce.
2. Zvolte tlačítko **Nastavení** tlačítko (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.
3. Na kartě **Nastavení pracovní vývěsky** v části **Povolit integraci s Broadbean** zapněte integraci.
4. Kontaktujte Broadbean a zadejte informace do **uživatelského jména, ID klienta a tokenu šifrování**.

> [!WARNING]
> Vaše přihlašovací údaje do Broadbean jsou citlivé a důvěrné. Proto je uchovávejte a sdílejte zodpovědně. Tyto údaje může zobrazit kdokoli, kdo má roli správce v aplikaci Attract.

> [!NOTE]
> Společnost Microsoft a Attract nejsou zahrnuty při vytváření a údržbě těchto hodnot. Je to vaše zodpovědnost udržovat je v aktuálním stavu v aplikaci Attract a pracovat s Broadbeanem na řešení problémů, které se týkají vašich přihlašovacích údajů.

### <a name="post-a-job-to-broadbean"></a>Publikování pracovního místa na Broadbean

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
2. V části **Publikování** zvolte tlačítko s třemi tečkami (**...**), které odpovídá Broadbeanu, a poté vyberte **Zobrazit**.

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

### <a name="troubleshoot-the-broadbean-integration"></a>Řešení problémů s integrací s Broadbean

Pokud máte problémy s publikováním pracovního místa na Broadbean, vyzkoušejte následující kroky.

1. Ověřte, zda jsou přihlašovací údaje Broadbean, které jste zadali v aplikaci Attract, platné a správné.
2. Pokud jsou přihlašovací údaje platné a správné, kontaktujte [Broadbean podporu](https://www.broadbean.com/resources/support/).
3. Pokud problém přetrvává, obraťte se na [podporu společnosti Microsoft](./talent-support.md).
