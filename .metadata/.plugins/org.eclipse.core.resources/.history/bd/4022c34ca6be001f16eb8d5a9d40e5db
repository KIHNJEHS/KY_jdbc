package com.java.study01;

import java.io.IOException;
import java.io.InputStream;

import org.apache.ibatis.io.Resources;
import org.apache.ibatis.session.SqlSession;
import org.apache.ibatis.session.SqlSessionFactory;
import org.apache.ibatis.session.SqlSessionFactoryBuilder;

public class App {

	public static void main(String[] args) {
		try {
			// 1. mybatis 환경 설정 파일 위치 변수
			String resource = "mybatis-config.xml";
			// 2. mybatis 설정 파일 읽기
			InputStream inputStream = Resources.getResourceAsStream(resource);
			// 3. 접속 정보 생성하기
			SqlSessionFactory sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);
			System.out.println("Factory Connection!!");
			// 4. 접속 정보를 통하여 하나의 통로 연결하기
			SqlSession session = sqlSessionFactory.openSession();
			// 5. 연결된 통로를 이용하여 SQL 실행하기
			int result =  session.selectOne("test.test1");
			System.out.println("Result : " + result);
		} catch (IOException e) {
			e.printStackTrace();
		}
	}

}
