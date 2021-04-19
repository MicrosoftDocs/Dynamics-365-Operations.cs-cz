---
title: Vytvoření funkčních míst
description: Toto téma vysvětluje, jak vytvořit funkční místa v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8bdf8367cb7a54520c671fbc05807b891e0cc45
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813838"
---
# <a name="create-functional-locations"></a>Vytvoření funkčních míst

[!include [banner](../../includes/banner.md)]

 

Toto téma vysvětluje, jak vytvořit funkční místa v modulu Správa majetku.

Po vytvoření struktury funkčního místa si uvědomte, že jakmile jste vytvořili funkční místo, nemůžete ho přesunout z původního místa. To znamená, že byste měli pečlivě zvážit strukturu funkčních míst předtím, než je začnete vytvářet v modulu Správa majetku. Pokud funkčního místa litujete, můžete je odstranit za předpokladu, že ještě nebylo použito.

Abyste mohli pracovat s funkčními místy, začněte vytvořením dvou "kategorií" funkčních míst:

- Vytvořte *jedno* výchozí funkční místo s žádnými dílčími umístěními. Toto funkční místo se používá pouze jako standardní umístění pro majetek při vytváření nového majetku.  
- Vytvořte struktury funkčních míst požadované pro správu prací údržby ve vaší firmě.

## <a name="create-a-default-functional-location"></a>Vytvoření výchozího funkčního místa

Při použití funkčních míst začněte vytvořením jednoho výchozího umístění, které bude použito při vytváření nového majetku. Toto funkční místo je to, které vyberete v poli **Správa majetku** > **Nastavení** > **Parametry správy majetku** > **Majetek** odkaz > **Výchozí funkční umístění**. Výchozí funkční místo lze použít při vytváření nového majetku v době, kdy jste pro majetek nenastavili strukturu funkčních míst.

1. Vyberte **Správa majetku** > **Společné** > **Funkční místa** > **Všechna funkční místa**.  
2. V poli **Všechna funkční místa** vyberte možnost **Nový**.
3. Zadejte ID do pole **Funkční místo**, například "0000" nebo "výchozí", což označuje, že se jedná o speciální funkční místo.
4. Do pole **Název** zadejte název výchozího funkčního místa.
5. *Nevybírejte* nadřazenou položku v poli **Nadřazený** – nechte toto pole prázdné.
6. V poli **typ funkčního umístění** vyberte typ funkčního umístění, které má být použito pro výchozí funkční umístění. Další [informace o nastavení](../setup-for-functional-locations/functional-location-types.md) typů funkčních míst naleznete v Typy funkčního místa.
7. Vyberte **OK**. Do tohoto funkčního místa byste neměli přidávat další data, protože jsou používána pouze jako dočasná lokace pro nový majetek, dokud nenainstalujete majetek do funkčních míst používaných vaší firmou.

## <a name="create-functional-locations"></a>Vytvoření funkčních míst

Následující procedura popisuje způsob vytvoření funkčních míst vyžadovaných pro správu údržby ve vaší firmě.

1. Vyberte **Správa majetku** > **Společné** > **Funkční místa** > **Všechna funkční místa**. Můžete vytvořit funkční místo ze zobrazení mřížky nebo podrobností.
2. Vyberte tlačítko **Nový**.
3. Zadejte ID do pole **Funkční místo**.
4. Do pole **Název** zadejte název výchozího funkčního místa.
5. Pokud je funkční místo dílčím místem ve struktuře, vyberte nadřazené místo v poli **nadřazené**.
6. Vyberte typ v poli **Typ funkčního místa**.
7. Vyberte **OK**.
8. Vyberte funkční místo a klikněte na tlačítko **Upravit** pro přidání dalších informací.

>[!NOTE]
>V závislosti na nastavení stavů životnosti funkčních míst může být nutné vytvořit všechna dílčí místa pro funkční místo a před zahájením instalace majetku změnit stav životnosti funkčního místa. Další informace o instalaci majetku najdete v části [Instalace majetku na funkčních místech](../functional-locations/install-objects-on-functional-locations.md). Další informace o nastavení stavů životního cyklu funkčního místa získáte v tématu [Stavy životního cyklu funkčního místa](../setup-for-functional-locations/functional-location-stages.md).

V zobrazení Podrobnosti se zobrazí pevné záložky, na které můžete přidat a na nichž můžete upravit informace o funkčním místě.

## <a name="general-information"></a>Obecné informace

Tato část obsahuje přehled nadřazených a podřízených informací ve struktuře funkčních míst. V části **podrobnosti** uvidíte počet atributů majetku, plánů údržby a majetku, které souvisejí s funkčním místem. V části **zásoby** můžete vybrat místo a sklad, ke kterým se funkční místo vztahuje. Místo a sklad se používají ve spojení s prognózami položek pracovního příkazu. Při vytváření prognózy položky se automaticky použijí informace o místě a skladu z funkčního místa majetku. V části **stav životního cyklu majetku** se zobrazují informace o stavu životního cyklu funkčního místa.

## <a name="installed-assets"></a>Nainstalovaný majetek

Další informace o instalaci majetku najdete v části [Instalace majetku na funkčních místech](../functional-locations/install-objects-on-functional-locations.md). K zobrazení více polí na této pevné záložce můžete použít tlačítko **Zobrazit**. Pole **Platné od** a **dílčí majetek** lze zobrazit v mřížce.

## <a name="asset-attribute-requirements"></a>Požadavky atributů majetku

Na této pevné záložce můžete přidat konkrétní požadavky na atributy pro majetek, který instalujete do funkčního umístění. Tyto požadavky jsou pouze informativní. Nebrání vám v instalaci majetku s jinými požadavky na atributy. Vyberte **Přidat řádek** a vyberte typ atributu. Potom zadejte příslušnou **hodnotu**, vyberete prahovou hodnotu v poli **kritéria prahové hodnoty** a záznam uložte.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Plány údržby a kola údržby

Zde můžete přidat plány údržby a kola údržby do funkčního místa včetně počátečního data. U majetku nainstalovaného ve funkčním místě mohou být nastaveny další plány údržby. Všechny plány údržby a kola údržby lze použít pro plánování položek kalendáře dlouhodobého majetku pro funkční místo a jeho aktuálně instalovaný majetek.

>[!NOTE]
>Pokud aktualizujete nastavení typů majetku, značek majetku a modelů majetku v plánech údržby na pevné záložce **Všechna funkční umístění** > **Plány údržby** po provedení plánovaných plánů údržby, existující položky plánu údržby vztahující se k tomuto funkčnímu umístění jsou automaticky odstraněny. Chcete-li vytvořit nové položky plánu, které odpovídají nastavení aktualizovaného plánu údržby na funkčním místě, musíte pro toto funkční místo spustit nový plán plánu údržby. 

## <a name="address"></a>Adresa

Zadejte adresu funkčního místa na pevnou záložku **Adresa**. Adresy na funkčních místech jsou zděděny, což znamená, že pokud dílčí místo nemá definovanou adresu, použije se adresa nadřazeného místa.

## <a name="workers"></a>Pracovníci

Na této pevné záložce můžete přidat zaměstnance, kteří jsou přidruženi k funkčnímu místu a můžete vybrat funkční místo jako primární pro pracovníka. 

## <a name="attributes"></a>Atributy

Na této pevné záložce můžete nastavit hodnoty pro atributy funkčních míst. Tyto atributy lze použít k popisu vlastností nebo charakteristik vztahujících se k funkčnímu místu, jako jsou například konstrukční vlastnosti, typ budovy, popisy oblastí nebo umístění nad nebo pod zemí.

Vyberte **Přidat řádek** a vyberte typ atributu. Dále vložte **hodnotu** vztahující se k typu atributu a uložte záznam.

## <a name="financial-dimensions"></a>Finanční dimenze

Můžete vybrat finanční dimenze pro funkční místo. [Typy](../setup-for-functional-locations/functional-location-types.md) funkčních míst lze nastavit tak, aby umožňovaly automatickou aktualizaci finančních dimenzí z funkčního místa. To znamená, že majetek instalovaný ve finanční dimenzi automaticky získá finanční dimenze pro funkční místo. To je užitečné, pokud chcete různá nákladová střediska, v závislosti na skladových místech.

Když jsou v nadřazeném funkčním místě aktualizovány dimenze **Místo**, **Sklad**, **Adres** a **Finance**, lze odpovídajícím způsobem aktualizovat související dílčí funkční místa, pokud tento výběr provedete během aktualizace. Otevře se dialogové okno, které vám poskytne možnosti aktualizace.

## <a name="copy-a-functional-location-structure"></a>Kopírování struktury funkčního místa

Pokud má vaše společnost několik funkčních míst s podobnými strukturami míst, můžete pomocí funkce kopírování v modulu Správa majetku rychle vytvořit řadu podobných hierarchií míst. Při kopírování určitého funkčního míst nebo celé struktury má nové místo nebo struktura stejný název jako ten, který jste zkopírovali. Po dokončení postupu kopírování můžete snadno změnit název nebo jiné nastavení na novém funkčním místě za předpokladu, že to umožní vybraný stav životnosti funkčního místa pro nové funkční místo.

1. V poli **Všechna funkční místa** vyberte funkční místo, které chcete kopírovat. Pokud například chcete zkopírovat celou strukturu funkčních místa včetně dílčích míst, vyberte nejvyšší místo (nadřazené).
2. Vyberte tlačítko **Kopírovat strukturu funkčního místa**. Místo, které jste vybrali na stránce se seznamem, je zobrazeno v poli **Kopírovat z**.
3. Zadejte název nového místa do pole **Nové funkční místo**.
4. V poli **Nadřazená položka k vložení pod** byste měli pouze zadat pouze ID nadřazené položky, pokud by vytvářené místo mělo být součástí existující struktury funkčních míst.
5. Klikněte na tlačítko **OK**. Nová struktura funkčního místa je zobrazena v poli **Všechna funkční místa**.

>[!NOTE]
>Když kopírujete strukturu funkčních míst, stavy životnosti funkčních míst v nové struktuře jsou nastaveny na první stav, který jste vytvořili pro funkční místo. To, zda můžete přejmenovat nebo odstranit funkční místo pomocí tlačítek **Přejmenovat** a **Odstranit** v části **Všechna funkční místa**, závisí na aktuálním stavu životního cyklu funkčního místa.

## <a name="delete-a-functional-location"></a>Vytvoření funkčního místa

Funkční místo se souvisejícími dílčími místo může být odstraněno, pokud nebyl nainstalován žádný majetek na některé z funkčních míst, která se pokoušíte odstranit, a pokud to umožňuje současný stav životnosti aktuálního funkčního místa.

1. V poli **Všechna funkční místa** vyberte funkční místo, které chcete odstranit.
2. V případě potřeby aktualizujte funkční místo na stav životnosti funkčního místa, který umožňuje odstranění funkčního místa.
3. Zvolte **Odstranit**.

>[!NOTE]
>Pokud nelze odstranit funkční místo, můžete místo toho zpracovat nastavením stavu životnosti funkčního místa pro tento účel. Můžete například nastavit fázi vyřazení nebo odstranění, která by neměla být aktivní fází, ve formuláři **Stavy životního cyklu funkčních míst**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]