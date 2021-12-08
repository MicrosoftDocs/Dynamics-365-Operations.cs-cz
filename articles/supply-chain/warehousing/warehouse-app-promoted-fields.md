---
title: Konfigurace propagovaných polí pro kroky v mobilní aplikaci Warehouse Management
description: Toto téma popisuje, jak propagovat a zvýraznit konkrétní informace pro libovolný krok v tocích úloh pro mobilní aplikaci Warehouse Management.
author: MarkusFogelberg
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 05ca38e366331c2132bb46eddf77ae2ef371256b
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678635"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Konfigurace propagovaných polí pro kroky v mobilní aplikaci Warehouse Management

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: GA with 10.0.23 -->

> [!IMPORTANT]
> Funkce, které jsou popsány v tomto tématu, platí pouze pro novou mobilní aplikaci Warehouse Management. Nemají vliv na starou skladovou aplikaci, která je nyní zastaralá.

Toto téma popisuje, jak propagovat a zvýraznit konkrétní informace pro libovolný krok v tocích úloh pro mobilní aplikaci Warehouse Management. Tato schopnost může pomoci zaměřit pozornost pracovníků na nejdůležitější oblasti při práci v toku. Pro každý krok v každém procesu mohou správci vybrat, která pole propagovat a která pole zvýraznit.

## <a name="enable-promoted-fields-in-your-system"></a>Aktivace propagovaných polí v systému

Než budete moci nastavit propagovaná pole, musíte provést následující postup, abyste povolili požadované funkce a vygenerovali požadované názvy polí v mobilní aplikaci Warehouse Management.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
1. V [pracovním prostoru **Správa funkcí**](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktivujte funkci, která je uvedena následovně:

    - **Modul:** *Řízení skladu*
    - **Název funkce:** *pokyny ke krokům aplikace Warehouse*

    Pro více informací o funkci *Pokyny pro krok aplikace Warehouse* viz [Přizpůsobení názvů kroků a pokynů pro mobilní aplikaci Warehouse Management](mobile-app-titles-instructions.md). Tato funkce je předpokladem pro funkci *Propagovaná pole Warehouse Management*.

1. Aktivujte funkci, která je zde uvedena, následujícím způsobem:

    - **Modul:** *Řízení skladu*
    - **Název funkce:** *Propagovaná pole aplikace Warehouse*

    Tato funkce je funkce popsaná v tomto tématu.

1. Aktualizujte názvy polí v mobilní aplikaci Warehouse Management tím, že přejdete na **Warehouse Management \> Nastavení \> Mobilní zařízení \> Názvy polí aplikace Warehouse** a vyberete **Vytvořit výchozí nastavení**. Další informace viz [Konfigurace polí pro mobilní aplikaci Řízení skladu](configure-app-field-names-priorities-warehouse.md).
1. Opakujte předchozí krok pro každou právnickou osobu (společnost), kde používáte mobilní aplikaci Warehouse Management.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Konfigurace propagovaných polí z přepsání specifického pro nabídku

Pomocí následujícího postupu nastavte propagovaná pole.

1. Vytvořte přepsání specifické pro nabídku pro příslušnou nabídku a krok, jak je popsáno v části [Přizpůsobení názvů kroků a pokynů pro mobilní aplikaci Warehouse Management](mobile-app-titles-instructions.md).
1. Najděte kombinaci hodnot **ID kroku** a **Názvu položky nabídky**, které chcete upravit, a vyberte hodnotu ve sloupci **ID kroku**.
1. Na stránce, která se objeví, na pevné záložce **Vybrat propagovaná pole** vyberte možnost **Vybrat pole** na panelu nástrojů.
1. V dialogovém okně **Propagovaná pole** vyberte pole, která chcete propagovat. Můžete také zvýraznit až dvě z vybraných polí. Zvýrazněná pole budou v mobilní aplikaci Warehouse Management zobrazena tučně. Při výběru polí vezměte v úvahu skutečnost, že některé obrazovky mohou být dostatečně velké, aby zobrazily pouze jedno nebo dvě propagovaná pole. Příklad, který ukazuje, jak tato nastavení používat, naleznete ve scénáři dále v tomto tématu.

    > [!NOTE]
    > Seznam **Dostupná pole** je omezen na pole, která se mohou objevit pro položku nabídky. O tom, zda se pole skutečně objeví v mobilní aplikaci Warehouse Management, však rozhodují další faktory (například složení položky). Pokud jste nakonfigurovali propagovaná pole, na hlavní stránce mobilní aplikace Warehouse Management se zobrazí pouze vybraná pole. Pracovníci však mohou stále zobrazit zbývající pole klepnutím na stránku podrobností.

1. Výběrem **OK** použijte nastavení. Vaše vybraná pole jsou nyní uvedena na pevné záložce **Vybrat propagovaná pole**.

## <a name="example-scenario"></a>Příklad

### <a name="enable-sample-data"></a>Povolit ukázková data

Chcete-li použít specifikované ukázkové záznamy a hodnoty k procházení tohoto scénáře, musíte používat systém, ve kterém jsou nainstalována standardní ukázková data. Dříve než začnete, musíte také vybrat právnickou osobu **USMF**.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Konfigurace vychystávání pomocí propagovaných kroků na kroku registrační značky

V tomto postupu nastavíte propagovaná a zvýrazněná pole pro položku nabídky **Prodejní vychystávání** v kroku registrační značky.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Kroky mobilního zařízení**.
1. Najděte pojmenované ID kroku *LicensePlateId* a vyberte ho.
1. V podokně akcí vyberte **Přidat konfiguraci kroku**.
1. V rozevíracím dialogovém okně použijte pole **Položka nabídky** k vyhledání a vybrání *Prodejní vychystávání*.
1. Vyberte **OK**.
1. Zobrazí se stránka podrobností pro přepsání, které jste právě vytvořili. Na pevné záložce **Vybrat propagovaná pole** vyberte možnost **Vybrat pole** na panelu nástrojů.
1. V dialogovém okně **Propagovaná pole** můžete vybrat pole, která chcete propagovat a zvýraznit. V seznamu **Dostupná pole** vyhledejte a vyberte následující pole a pomocí tlačítek je přesuňte do seznamu **Vybraná pole**:

    - Umístění
    - Položka
    - Název produktu
    - Stav skladu

1. Pomocí tlačítek se šipkou nahoru a šipkou dolů upravte pořadí polí v seznamu **Vybraná pole**. V mobilní aplikaci Warehouse Management se pole zobrazí v pořadí, které zde nastavíte.
1. Vyberte pole **Umístění** a pak vyberte **Zvýraznit**.
1. Výběrem tlačítka **OK** konfiguraci uložte.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Zobrazení propagovaných polí pro kroky v mobilní aplikaci Warehouse Management

V tomto postupu otevřete mobilní aplikaci Warehouse Management a projdete kroky k zobrazení polí, která jste propagovali a zvýraznili v předchozím postupu.

1. V Microsoft Dynamics 365 Supply Chain Management vytvořte prodejní objednávku, která bude vyžadovat krok vyskladnění k odběru z místa, které je sledována registrační značka. Poté vydejte prodejní objednávku do skladu. Poznamenejte si vygenerované ID práce.
1. Otevřete mobilní aplikaci Warehouse Management a přihlaste se do skladu 24. (Ve standardních ukázkových datech se přihlaste pomocí čísla *24* ID uživatele a *1* jako heslo.)
1. Vyberte nabídku **Odchozí** a poté vyberte položku nabídky **Prodejní vychystávání**.
1. Postupujte podle pokynů pro zadávání dat na obrazovce a zadejte ID práce, které bylo vygenerováno v kroku 1.
1. Na kroku, který obsahuje text **Naskenovat registrační značku**, byste měli vidět změny, které jste provedli na stránce podrobností. Pole se zobrazí v pořadí, které jste nastavili pro propagovaná pole, a pole **Umístění** je zobrazeno tučně.