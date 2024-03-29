---
title: Konfigurační klíče a datové entity
description: Tento článek popisuje vztah mezi konfiguračními klíči a entitami dat.
author: peakerbl
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 8083c8c053197f685985f340281c43f30053d2a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885255"
---
# <a name="configuration-keys-and-data-entities"></a>Konfigurační klíče a datové entity

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Před použitím datových entit k importu nebo exportu dat doporučujeme nejprve určit dopadu konfiguračních klíčů na datové entity, které chcete použít.

Další informace o konfiguračních klíčích naleznete v části [Licenční kódy a sestavy konfiguračních klíčů](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Přiřazení konfiguračních klíčů
Konfigurační klíče lze přiřadit k jednomu nebo všem následujícím artefaktům.

- Datové entity
- Tabulky použité jako datové zdroje
- Pole tabulky
- Pole datových entit

Následující tabulka shrnuje, jak hodnoty konfiguračních klíčů na různých artefaktech, které jsou základem objektu, mění očekávané chování objektu.

| Nastavení konfigurační klíče na datové entitě | Nastavení konfigurační klíče na tabulce | Nastavení konfigurační klíče na poli tabulky | Konfigurační klíč na poli datové entity | Očekávané chování |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| Zakázaný                                | Nehodnoceno                      | Nehodnoceno                            | Nehodnoceno                          | Je-li konfigurační klíč pro datovou entitu zakázán, nebude datová entita funkční. Není důležité, zda jsou povoleny nebo zakázány konfigurační klíče v podkladových tabulkách a polích. |
| Povoleno                                 | Zakázaný                           | Nehodnoceno                            | Nehodnoceno                          | Pokud je povolen konfigurační klíč pro entitu dat, platforma správy dat zkontroluje konfigurační klíč na každé podkladové tabulce. Pokud je konfigurační klíč pro tabulku zakázán, tabulka nebude v datové entitě dostupná pro funkční použití. Je-li konfigurační klíč tabulky zakázán, tabulka a nastavení konfiguračního klíče datové entity nejsou vyhodnocovány. Má-li primární tabulka v entitě svůj konfigurační klíč zakázán, systém se bude chovat, jako kdyby byl konfigurační klíč entity zakázán. |
| Povoleno                                 | Povoleno                            | Zakázaný                                 | Nehodnoceno                          | Pokud je povolen konfigurační klíč pro datovou entitu a konfigurační klíce podkladových tabulek jsou povoleny, platforma správy dat zkontroluje konfigurační klíč na polích v tabulkách. Jestliže je konfigurační klíč pro pole zakázán, toto pole nebude k dispozici v datové entitě pro funkční použití, a to i v případě, že odpovídající pole datové entity má povolený konfigurační klíč. |
| Povoleno                                 | Povoleno                            | Povoleno                                  | Zakázaný                               | Pokud je povolen konfigurační klíč na všech ostatních úrovních, ale konfigurační klíč pole entity není povolen, nebude pole nebude k dispozici pro použití v datové entitě. |

> [!NOTE]
> Má-li entita jinou entitu jako zdroj dat, jsou použity výše uvedené sémantiky rekurzivním způsobem.

### <a name="entity-list-refresh"></a>Obnovení seznamu entit
Při obnovení seznamu entit vytvoří platforma správy dat metadat konfiguračního klíče pro použití za běhu. Tato metadata jsou vytvořena pomocí výše uvedené logiky. Důrazně doporučujeme počkat na dokončení obnovy seznamu entit před použitím úloh a entit v platformě správy dat. Pokud nepočkáte, metadata konfiguračního klíče nemusí být aktuální a mohou mít za následek neočekávané výsledky. Při obnově seznamu entit se zobrazí na stránce seznamu entit následující zpráva.

![Obnovení seznamu entit.](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Stránka seznamu datových entit
Stránku seznamu datových entit v pracovním prostoru Správa dat zobrazuje nastavení konfiguračního klíče pro entity. Začněte touto stránkou pro pochopení dopadu konfiguračních klíčů na datové entity.

Tyto informace se zobrazí pomocí metadat, která jsou vytvořena během obnovení entity. Sloupec konfiguračního klíče zobrazuje název konfiguračního klíče, který je přidružena k datové entitě. Pokud je tento sloupec prázdný, znamená to, že neexistuje konfigurační klíč přidružený k datové entitě. Sloupec stavu konfiguračního klíče zobrazuje stav konfiguračního klíče. Pokud je zaškrtnutý, znamená to, že je tento klíč povolen. Pokud je prázdný, je klíč buď zakázán nebo neexistuje žádný přidružený klíč.

![Stránka seznamu entit.](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Cílová pole
Dalším krokem je přechod na podrobnosti datové entity k zobrazení dopadu konfiguračních klíčů na tabulky a pole. Formulář cílových polí pro datovou entitu zobrazuje konfigurační klíč a informace o stavu klíče pro související tabulky a pole v datové entitě. Má-li samotná datová entita svůj konfigurační klíč zakázán, zobrazí se zpráva s upozorněním, že tabulky a pole ve formuláři cílových polí pro tuto entitu nebudou vůbec k dispozici, bez ohledu na stav konfiguračních klíčů.

![Cílová pole.](./media/Target_fields_1.png)

### <a name="child-entities"></a>Podřízené entity 
Některé entity mají další entity jako zdroje dat, nebo se jedná o složené datové entity: informace o konfiguračním klíči pro tyto entity jsou zobrazené ve formuláři podřízených entit. Použijte tento formulář stejným způsobem na stránku seznamu entit uvedenou výše. Formulář cílových polí pro podřízené entity se rovněž chová tak, jak je popsáno výše.

![Cílová pole.](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Použití datových entit
Po porozumění celému dopadu, pokud nějaký je, konfiguračních klíčů na datové entity, které chcete použít, nyní můžete přejít k použití datových entit pomocí jejich přidání do datových projektů. 

### <a name="run-time-validations-for-configuration-keys"></a>Ověření za běhu pro konfigurační klíče
S použitím metadat konfiguračního klíče vytvořeného během seznamu obnovení entit jsou prováděna ověření za běhu v následujících případech použití.

- Při přidání datové entity do úlohy
- Při kliknutí uživatele na tlačítko Ověřit na seznamu entit
- Když uživatel načte datový balíček do datového projektu
- Když uživatel načte šablonu do datového projektu
- Když je načten existující datový projekt
- Když se načte šablona do datového projektu
- Před provedením exportu/importu (dávky, bez dávky, periodický, OData)
- Když uživatel vytvoří mapování
- Když uživatel mapuje pole v mapování uživatelského rozhraní
- Když uživatel přidá pouze importovatelná pole.

### <a name="managing-configuration-key-changes"></a>Správa změn konfiguračních klíčů
Kdykoli aktualizujete konfigurační klíče na entitě, úrovni tabulek nebo polí, seznam entit v platformě správy dat musí být aktualizován. Tento proces zajišťuje, aby platforma vzala nejnovější nastavení konfiguračního klíče. Dokud nebude obnoven seznam entit, bude se zobrazovat na stránce seznamu entit následující upozornění. Aktualizované změny konfiguračního klíče se projeví okamžitě po aktualizaci seznamu entit. Doporučujeme ověřit existující datové projekty a úlohy, abyste se ujistili, že fungují podle očekávání poté, co změny konfiguračních klíčů začaly být účinné.

![Cílová pole.](./media/Target_fields_3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
