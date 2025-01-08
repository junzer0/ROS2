# ROS 2
2025 ETRI Internship Study Note

### ROS 2 특징
- 크로스 플랫폼(Cross-platform)
- 실시간성(Real-Time)
  - DDS(Data Distribution Service) 지원
    - RTPS(Real-Time Publish-subscribe Protocol) 사용
- 보안성(Security)
  - DDS-Security
- 통신(Communication)
  - DDS –> IDL(Interface Description Language) 지원 
  - QoS(Quality of Service) - 노드간 통신 지원
- 미들웨어 인터페이스(Middleware Interface)
  - ROS2에서는 RMW(ROS Middleware) 형태로 지원
- Node manager(Discovery)
  - Dynamic Discovery 이용 –> DDS 미들웨어를 통해 노드를 직접 검색하여 연결 가능
- Language
  - C++14(C++17)
  - Python3.5+
- Build system
  - ament 이용(ROS1 catkin의 업그레이드 버전) - python 패키지도 관리 가능
- Build tools
  - ament tools
  - colcon(collective construction) -> ROS2 패키지 작성, 테스트, 빌드, 등을 지원
- Build options
  - Multiple workspace 
	- ROS1에서는 catkin_ws와 같이 특정 워크스페이스를 확보하고 하나의 워크스페이스에서 모든 작업을 진행, ROS2에서는 복수의 독립된 워크스페이스를 사용할 수 있어서 작업 목적 및 패키지 종류별로 이를 관리할 수 있게 됨
  - No non-isolated build
	- ROS1에서는 하나의 CMake 파일로 여러 개의 패키지를 동시에 빌드할 수 있었음. -> 빌드 속도는 빨라지지만, 모든 패키지의 종속성에 신경을 많이 써야 하고 빌드 순서가 매우 중요하게 됨. 또한 모든 패키지가 동일 네임스페이스를 사용하게 되므로 이름 충돌이 발생할 수 있음 ROS2에서는 catkin_make_isolated 형태와 같은 격리 빌드만을 지원 -> 모든 패키지를 별도로 빌드, 설치용 폴더를 분리하거나 병합할 수 있게 됨
  - No devel space
	- 패키지를 빌드한 후 설치해야 패키지를 사용할 수 있도록 변경 
- Version control system
  - vcstool을 통해 버전 관리(ROS1, ROS2 둘 다 지원)
- Client library
  - rclcpp, rclc, rclpy, rcljava, rclobjc, rclada 등 지원
- Lifecycle
  - 노드의 상태 모니터링 및 천이 가능 
- Multiple nodes
- Treading model
- Messages(Topic, Service, Action)
- Command Line Interface
- Launch
- Graph API
- Embedded System

### ROS 2와 DDS
