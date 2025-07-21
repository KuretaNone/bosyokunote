---
id: 橋梁点検-Libexpad
aliases:
  - 橋梁点検-Libexpad
tags: []
created: "2025-05-28"
updated: "2025-05-28"
---

# 橋梁点検-Libexpad
[[橋梁点検支援作図システムで使用しないdll]]
## 使用しない処理
procedure XMLSetAttlistDeclHandler;
procedure XMLSetXmlDeclHandler;
function  XMLParserCreate;
function  XMLParserCreateNS;
function  XMLParserCreateMM;
function XMLParserReset;
procedure XMLSetEntityDeclHandler;
procedure XMLSetElementHandler;
procedure XMLSetStartElementHandler;
procedure XMLSetEndElementHandler;
procedure XMLSetCharacterDataHandler;
procedure XMLSetProcessingInstructionHandler;
procedure XMLSetCommentHandler;
procedure XMLSetCdataSectionHandler;
procedure XMLSetStartCdataSectionHandler;
procedure XMLSetEndCdataSectionHandler;
procedure XMLSetDefaultHandler;
procedure XMLSetDefaultHandlerExpand;
procedure XMLSetDoctypeDeclHandler;
procedure XMLSetStartDoctypeDeclHandler;
procedure XMLSetEndDoctypeDeclHandler;
procedure XMLSetUnparsedEntityDeclHandler;
procedure XMLSetNotationDeclHandler;
procedure XMLSetNamespaceDeclHandler;
procedure XMLSetStartNamespaceDeclHandler;
procedure XMLSetEndNamespaceDeclHandler;
procedure XMLSetNotStandaloneHandler;
procedure XMLSetExternalEntityRefHandlerArg;
procedure XMLSetSkippedEntityHandler;
procedure XMLSetUnknownEncodingHandler;
function XMLSetParamEntityParsing;
procedure XMLDefaultCurrent;
procedure XMLSetReturnNSTriplet;
procedure XMLSetUserData;
function  XMLSetEncoding;
procedure XMLUseParserAsHandlerArg;
function  XMLSetBase;
function  XMLGetBase;
function  XMLGetSpecifiedAttributeCount;
function  XMLGetIdAttributeIndex;
function  XMLParse;
function  XMLGetErrorCode;
function  XMLGetBuffer;
function  XMLParseBuffer;
function  XMLExternalEntityParserCreate;
function  XMLGetCurrentLineNumber;
function  XMLGetCurrentColumnNumber;
function  XMLGetCurrentByteIndex;
function  XMLGetCurrentByteCount;
function  XMLGetInputContext;
procedure XMLParserFree;
function  XMLErrorString;
function  XMLExpatVersion;

## functionには引数が必要
## TXMLExternalEntityRefHandler
This is called for a reference to an external parsed general entity.
The referenced entity is not automatically parsed.
The application can parse it immediately or later using
XMLExternalEntityParserCreate.
The Parser argument is the Parser parsing the entity containing the reference;
it can be passed as the Parser argument to XMLExternalEntityParserCreate.
The systemId argument is the system identifier as specified in the entity declaration;
it will not be null.
The base argument is the system identifier that should be used as the base for
resolving systemId if systemId was relative; this is set by XMLSetBase;
it may be null.
The publicId argument is the public identifier as specified in the entity declaration,
or null if none was specified; the whitespace in the public identifier
will have been normalized as required by the XML spec.
The context argument specifies the parsing context in the format
expected by the context argument to
XMLExternalEntityParserCreate; context is valid only until the handler
returns, so if the referenced entity is to be parsed later, it must be copied.
The handler should return 0 if processing should not continue because of
a fatal error in the handling of the external entity.
In this case the calling Parser will return an XML_ERROR_EXTERNAL_ENTITY_HANDLING
error.
   Note that unlike other handlers the first argument is the Parser, not UserData.
