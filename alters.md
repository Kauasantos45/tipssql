

/* RENOMEIA A COLUNA */

EXEC sp_rename 'table_name.column_name', 'column_name_New', 'COLUMN';

 

/* CRIA UMA NOVA COLUNA NA TABELA */

ALTER TABLE table_name ADD column_name data_type;

 

/* ALTERA O TIPO  DE DADOS DE UMA COLUNA */

ALTER TABLE tblCampanhaComercial ALTER COLUMN ObjetivoTotal DECIMAL (18,2);

 

/* ALTERA A COLUNA PARA NULL OU NOT NULL */

ALTER TABLE tblCampanhaComercial ALTER COLUMN ObjetivoTotal DECIMAL(18,0) NOT NULL;

 

/* CRIA CHAVE ESTRANGEIRA */

ALTER TABLE tblCampanhaComercial

ADD CONSTRAINT FK_tblCampanhaComercial_TipoValor FOREIGN KEY (TipoValor)

REFERENCES tblCampanhaComercialTipoValor (TipoValor)

 

/* CRIA CHAVE PRIMARIA */

ALTER TABLE tblCampanhaComercialTipoValor

ADD CONSTRAINT PK_tblCampanhaComercialTipoValor_TipoValor PRIMARY KEY (TipoValor)

 

/* CRIA CHAVE COMPOSTA */

ALTER TABLE tblCampanhaComercialTipoValor

ADD CONSTRAINT PK_C_tblCampanhaComercialTipoValor_TipoValor PRIMARY KEY (TipoValor,TipoValor2)

 

/* EXCLUI CHAVE DA TABELA */

ALTER TABLE dbo.DocExe DROP CONSTRAINT FK_Column_B;

 

/* EXCLUI COLUNA DA TABELA */

ALTER TABLE dbo.doc_exb DROP COLUMN column_b;

 
