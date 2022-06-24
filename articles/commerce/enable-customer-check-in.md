---
title: Povolit oznámení o přihlášení zákazníka v místě prodeje (POS)
description: Tento článek popisuje, jak povolit oznámení o přihlášení zákazníka v místě prodeje Microsoft Dynamics 365 Commerce (POS).
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ae53657c95128eae793f670bd9dbc31d9fac0fe4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885138"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Povolit oznámení o přihlášení zákazníka v místě prodeje (POS)

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak povolit oznámení o přihlášení zákazníka v místě prodeje Microsoft Dynamics 365 Commerce (POS).

Ve svých e-mailech „objednávka je připravena k vyzvednutí“ mohou organizace poskytnout odkaz nebo tlačítko, které zákazníkům umožní upozornit obchod, že jsou v areálu a čekají, až jim bude doručen jejich balíček. Zákazníci poté obdrží potvrzení o přihlášení a obchod obdrží oznámení jako úkol ve své aplikaci POS. Tento úkol slouží jako výzva prodejnímu pracovníkovi k doručení objednávky do vozidla zákazníka. Zákazník tedy nemusí vstoupit do obchodu.

Workflow přihlášení zákazníka lze také nakonfigurovat tak, aby shromažďoval od zákazníků další informace, například číslo jejich parkovacího místa, značku, model a barvu jejich vozidla a pokyny k dodání. Obsluha obchodu může tyto informace použít k usnadnění plnění objednávky.

## <a name="enable-customer-check-in"></a>Aktivace přihlášení zákazníka

Když je zapnuta funkce přihlášení zákazníka, vygeneruje Commerce ID potvrzení objednávky (označované také jako referenční číslo kanálu). Také generuje ID potvrzení objednávky pro objednávky, které jsou vytvořeny prostřednictvím prodejních míst (POS) nebo kanálů call centra. 

Chcete-li zapnout funkci přihlášení zákazníka v centrále Commerce, postupujte následovně.

1. Přejděte na **Pracovní prostory \> Správa funkcí**.
2. Vyhledejte funkci **Vygenerovat konzistentní formát ID referenčního kanálu napříč kanály**. 
3. Vyberte funkci a poté v podokně vlastností vyberte možnost **Povolit nyní**. 

## <a name="create-a-check-in-confirmation-page"></a>Vytvořte stránku s potvrzením přihlášení

Na svém webu elektronického obchodu musíte vytvořit novou stránku, která bude sloužit jako prostředí pro potvrzení přihlášení. Prostřednictvím další konfigurace může stránka také obsahovat formulář, který shromažďuje další informace od zákazníků, aby se usnadnilo plnění objednávky. Informace o tom, jak nastavit stránku a modul, najdete v části [Modul přihlášení zákazníka](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Konfigurace šablony transakčního e-mailu

Musíte přidat odkaz nebo tlačítko **Jsem tady** na šablonu pro transakční e-mail, který zákazníci obdrží, když je jejich objednávka připravena k vyzvednutí. Tímto odkazem nebo tlačítkem zákazníci upozorní obchod, že dorazili, aby si vyzvedli objednávku. 

Přidejte odkaz nebo tlačítko na šablonu, která je namapována na typ oznámení **Balení dokončeno** a způsob doručení, který používáte k plnění objednávky. V šabloně vytvořte odkaz nebo tlačítko HTML, které odkazuje na adresu URL stránky s potvrzením přihlášení, kterou jste vytvořili, a které obsahuje názvy a hodnoty parametrů, jak je znázorněno v následujícím příkladu.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Další informace o konfiguraci e-mailových šablon najdete v tématu [Přizpůsobení transakčních e-mailů podle způsobu doručení](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>V POS je vytvořena úloha potvrzení odbavení

Poté, co zákazník oznámí prodejně, že je přítomen k vyzvednutí, na stránce odbavení se zobrazí potvrzovací zpráva a volitelný QR kód, který obsahuje ID potvrzení objednávky zákazníka. Zároveň je vytvořen úkol v seznamu úkolů v POS pro prodejnu, kde si zákazník objednávku vyzvedává. Tento úkol obsahuje všechny informace o zákazníkovi a objednávce, které jsou nutné pro splnění objednávky. V poli s pokyny úkolu zobrazují všechny informace, které byly od zákazníka shromážděny prostřednictvím formuláře s doplňujícími informacemi.

## <a name="end-to-end-testing"></a>Komplexní testování

Přihlášení zákazníka vyžaduje, aby byly konkrétní parametry a hodnoty předány přihlašovací stránce a poté rozhraní API pro přihlášení zákazníka. Nejjednodušší přístup je proto otestovat funkci v prostředí, kde lze vytvořit a zabalit testovací objednávku. Tímto způsobem lze vygenerovat e-mail s „objednávkou připravenou k vyzvednutí“, který má adresu URL obsahující požadované názvy a hodnoty parametrů.

Chcete-li otestovat funkci přihlášení zákazníka, postupujte takto.

1. Vytvořte stránku pro přihlášení zákazníka a poté přidejte a nakonfigurujte modul pro přihlášení zákazníka. Více informací viz [Odbavení pro modul vyzvednutí](check-in-pickup-module.md). 
1. Vraťte stránku se změnami, ale nepublikujte ji.
1. Přidejte následující odkaz na šablonu e-mailu, která je vyvolána typem oznámení o dokončení balení pro způsob doručení vyzvednutí. Další informace viz [Vytvoření e-mailových šablon pro transakční události](email-templates-transactions.md).

    - **Pro předprodukční (UAT) prostředí:** Přidejte fragment kódu z části [Nakonfigurujte šablonu transakčního e-mailu](#configure-the-transactional-email-template) výše v tomto článku.
    - **Pro produkční prostředí:** Přidejte následující komentovaný kód, aby to neovlivnilo stávající zákazníky.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Vytvořte objednávku, kde je specifikován způsob doručení vyzvednutí.
1. Když obdržíte e-mail, který se spouští typem oznámení o dokončení balení, otestujte tok přihlášení otevřením stránky pro přihlášení s adresou URL, kterou jste přidali dříve. Protože adresa URL obsahuje příznak `&preview=inprogress`, před zobrazením stránky budete vyzváni k ověření.
1. Zadejte jakékoli další požadované informace ke konfigurace modulu.
1. Ověřte, že se zobrazení potvrzení přihlášení zobrazuje správně.
1. Otevřete terminál POS obchodu, kde bude objednávka vyzvednuta.
1. Vyberte dlaždici **Objednávky k vyzvednutí** a ověřte, že se objednávka zobrazuje.
1. Ověřte, že se v podokně podrobností zobrazují všechny další informace, které byly nakonfigurovány v modulu přihlášení.

Poté, co ověříte, že funkce přihlášení zákazníka funguje od začátku do konce, postupujte takto.

1. Publikujte stránku přihlášení.
1. Pokud testujete v produkčním prostředí, odkomentujte adresu URL v e-mailové šabloně „objednávka připravena k vyzvednutí“, aby se zobrazil odkaz nebo tlačítko **Jsem tady**. Poté šablonu znovu nahrajte.

## <a name="additional-resources"></a>Další prostředky

[Přihlášení k modulu vyzvednutí](check-in-pickup-module.md)

[Přizpůsobení transakčních e-mailů podle způsobu doručení](customize-email-delivery-mode.md)

[Vytvoření e-mailových šablon pro transakční události](email-templates-transactions.md)
